- ### Roam JS 
    [Roam JS Charts](https://roamjs.com/docs/extensions/charts) 
    [Roam JS Tag Cycle](https://roamjs.com/docs/extensions/tag-cycle)
        - [[roam/js/tag-cycle]]
    {{[[roam/js]]}}
        - ```javascript
var installScript = name => {
  var existing = document.getElementById(name);
  if (existing) {
    return;
  }  
  var extension = document.createElement("script");      
  extension.type = "text/javascript";
  extension.src = `https://roamjs.com/${name}.js`;
  extension.async = true;
  extension.id = name;
  document.getElementsByTagName("head")[0].appendChild(extension);
};
installScript("charts");
installScript("tag-cycle");```
- ### Roam 42
    - https://roam42.com 
    - {{{[[roam/js]]}}}
        - ```javascript
var s = document.createElement('script');
	s.type = "text/javascript";
  	s.src =  "https://roam42.glitch.me/main.js";
  	s.async = true;
document.body.appendChild(s);```
- ### Sentiment analysis
    - Use with Template/Sentiment used by [[template/Customer Feedback]]
    - {{[[roam/js]]}}
        - ```javascript
if (typeof window.afinn == 'undefined') {
    var s = document.createElement('script');
    s.type = "text/javascript";
    s.src =  "https://zsviczian.github.io/afinn_en.js";
    s.async = false;
    document.getElementsByTagName('head')[0].appendChild(s);
}

window.SentimentAnalysis = {
  tokenize(text) {return text.toLowerCase().split(' ');},
  deleteUselessChars(word) {return word.replace(/[^\w]/g,'');},
  rateWord(word) {return (word in window.afinn) ? window.afinn[word] : 0;},
  sum(x, y) {return x+y;},
  analyze(text) {
    return this.tokenize(text)
               .map(this.deleteUselessChars)
               .map(this.rateWord)
               .reduce(this.sum);
  }
}```
- ### Datomic Query Common functions
    - {{[[roam/js]]}}
        - ```javascript
window.datomicQuery = {
  MAXROWS: 40,
  reg_fields_string: null,
  reg_fields: null,
  reg_field: null,
  reg_is_pull: null,
  field_names: [],
  output: '',
  overwriteBlockUID: null, //this is the UID of the previous result set
  init() {
    this.reg_fields_string = new RegExp(/\:find\s+(.+)/);
    this.reg_fields        = new RegExp(/(\?[^\s]+|\(pull.+\))/g);
    this.reg_field         = new RegExp(/\?([\w\d]+)\:?([\w\d]+)?/);
    this.reg_is_pull       = new RegExp(/(\(.+\))/);//(\(\s?pull.+\))
  },
  
  //Helper functions to get clickeable links
  getLocation(uid) {
    if (window.location.href.includes('/page/')) 
      return window.location.href.substring(window.location.origin.length+1,window.location.href.length-9)+uid;
    else
      return window.location.href.substring(window.location.origin.length+1,window.location.href.length)+'/page/'+uid
  },
  pageLink(title, uid) {
    return `[:a {:class "rm-page__title", :href "${this.getLocation(uid)}"} "${title}"]`;
  },
  toTwoDigits(number) {
    return  ("0" + number).slice(-2);
  },
  msToDate(ms) {
    dt = new Date(ms);
    month = this.toTwoDigits(dt.getMonth()+1);
    day = this.toTwoDigits(dt.getDate());
    year = dt.getFullYear();
    uid = [month,day,year].join('-');
    title = [year, month, day].join('-');
    return this.pageLink(title,uid);
  },

  //In the end only the "quotation mark" needs an escape character due to hiccup
  encodeString(s){ 
    return s.replace(/["]/g, function(i) {
      return '\\"';
    });
  },

  //Helper function to check if variable is a dictionary object
  isDict(v) {
    return typeof v==='object' && v!==null && !(v instanceof Array) && !(v instanceof Date);
  },

  //recursive function to process the result set tree
  printResult(o,new_lines) {
    //Dictionary
    if (this.isDict(o)) {
      s = '[:table {:class "detail"} [:tbody ';
      for (var key in o) {
        val = o[key];
        if (key == 'title') 
          if (o['uid'] !== undefined)
            val = this.pageLink(val,o['uid']);
        if (key == 'time') 
          val = this.msToDate(o[key]);
        s += `[:tr [:td {:class "key"} "${key}"][:td {:class "val"} ${(o[key] != val) ? val : this.printResult(val,new_lines)}]]`;
      }
      return s+']]';
    }
    //Array
    else if (o instanceof Array) {  
  	  s = (new_lines) ? '[:table [:tbody ' : '';
      for (let i=0;i<this.MAXROWS/4 && i<o.length;i++) {
      //for (e of o) {       
      	s += ((new_lines) ? '[:tr {:class "' +(i%2 ? 'even val"}':'odd val"}') : '[:td {:class "val"}') + this.printResult(o[i],!new_lines)+']';
      }
      return s + ((new_lines) ? ']]' : '');
    }
    //Value
    else
      if (o != null) 
      	return '"' + this.encodeString(o.toString()) + '"';
      else 
        return '""';
  },
  clearPrevious() {
    let uid = document.activeElement.id.slice(-9);
    let children = window.roamAlphaAPI.q(`[:find ?uid ?order
                                           :where
									       [?b :block/uid "${uid}"]
									       [?b2 :block/parents ?b]
									       [?b2 :block/uid ?uid]
								     	   [?b2 :block/order ?order]]`).sort((a, b) => a[1] - b[1]);
    for (let i=1;i<children.length;i++) 
      roam42.common.deleteBlock(children[i][0]);
    this.overwriteBlockUID = (children.length>0) ? children[0][0] : null; //store UID of block to overwrite with result
  },
  getParentBlock() {
    let uid = document.activeElement.id.slice(-9);
    return s = window.roamAlphaAPI.q(`[:find ?s
  								:in $ ?uid
  								:where 
  								[?b :block/uid ?uid]
  								[?p :block/children ?b]
								[?p :block/string ?s]]`,uid);
  }, 

  buildTableHeader(query) {
    this.output = ':hiccup [:div {:class "scroller dont-focus-block"}  [:table [:tbody [:tr ';
    this.field_names = [];    
    let fields = Array.from(query.match(this.reg_fields_string)[1].matchAll(this.reg_fields));
	for (var f of fields) 
      if (f[0].match(this.reg_is_pull) != null) 
        this.field_names.push([f[0],'pull']);
      else {
        m = f[0].match(this.reg_field);
      this.field_names.push([m[1],(m[2] === undefined) ? '':m[2]]);
    }
    this.field_names.forEach(function(field,i) { 
      if (field[1]!='uid') 
        window.datomicQuery.output += '[:td {:class "head"} "'+field[0]+'"]';
    });
    this.output += ']';
  },
  writeBlock(message) {
    if (this.overwriteBlockUID!=null)
      roam42.common.updateBlock(this.overwriteBlockUID, message);
    else
      roam42.common.createBlock(document.activeElement.id.slice(-9), 0, message);   
  },
  processResults(results,query,writeblock = true) {
    query = query.replaceAll('\n',' ').replace(':in','\n:in').replace(':where','\n:where');
    this.buildTableHeader(query);
    //The first two levels are handled differently to enable processing of page links at the top level
    for (let i=0;i<this.MAXROWS && i<results.length;i++) {
      let title = '';
      this.output += '[:tr {:class "' +(i%2 ? 'even"}':'odd"}');
      this.field_names.forEach(function(fn,j) {
        switch(fn[1]) {
          case 'name': title = results[i][j]; break;
          case 'uid' : window.datomicQuery.output +=  '[:td {:class "val"}' + window.datomicQuery.pageLink(title, results[i][j]) +']'; break;
          case 'date': window.datomicQuery.output +=  '[:td {:class "val"}' + window.datomicQuery.msToDate(results[i][j]) +']';   + ']'; break;  
          default:     window.datomicQuery.output +=  '[:td {:class "val"}' + window.datomicQuery.printResult(results[i][j],false) +']'; 
        }
      });
      this.output += ']';
    }
    if (writeblock) 
      this.writeBlock(this.output + ']]]');
    return this.output + ']]]';
  }
}

window.datomicQuery.init();
let css = window.document.styleSheets[0];
css.insertRule('table.detail { width:100%; border-style: solid; border-width: thin; }', css.cssRules.length);
css.insertRule('td.key { padding-right: 10px; filter: brightness(110%); vertical-align: top; }', css.cssRules.length);
css.insertRule('td.head { padding-right: 10px; background-color: rgba(0,0,0,0.15); filter: brightness(120%); font-weight: 800; vertical-align: top; }', css.cssRules.length);
css.insertRule('td.val { padding-right: 10px; vertical-align: top; }', css.cssRules.length);
css.insertRule('tr.odd { background: rgba(255,255,255,0.05); vertical-align: top; }', css.cssRules.length);
css.insertRule('tr.even { background-color: rgba(0,0,0,0.05); vertical-align: top;}', css.cssRules.length);
css.insertRule('div.scroller { width: 100%; max-height: 500px; overflow-y: hidden; overflow: auto; }', css.cssRules.length);```
- ### [[(i) RoamAgile]]
    - {{[[roam/js]]}}
        - ```javascript
window.roamAgile = {
  TEAM_PAGE        : 'roamAgile/team', //has list of team members in separate blocks
  STORY_NAMESPACE  : 'story/',
  SPRINT_NAMESPACE : 'sprint/',
  BACKLOG_PAGE     : 'Backlog',
  SPRINTPLAN_BLOCK : 'Sprint Plan', //block starts-with, on sprint page, in sprint tempate
  BURNDOWN_BLOCK   : 'Burn Down', //block starts-with, on sprint page, in sprint tempate
  ESTIMATE_ATTRIB  : 'Estimate::',
  ASSIGNEDTO_ATTRIB: 'Assigned to::',
  STATUS_ATTRIB    : 'Status::',
  STATUS_ACTIVE    : 'status/active',
  STATUS_DRAFT     : 'status/draft',
  STATUS_CLOSED    : 'status/closed',
  async sleep(ms) { return new Promise(resolve => setTimeout(resolve, ms));},
  async getActiveSprint() {
    let activesprint_q = `[:find ?title:name 
 						   :where [?page :node/title ?title:name]
                                  [(clojure.string/starts-with? ?title:name "${this.SPRINT_NAMESPACE}")]
		                          [?block :block/page ?page]
 		                          [?active :node/title "${this.STATUS_ACTIVE}"]
 		                          [?block :block/refs ?active]
 		                          [?block :block/string ?status]
 		                          [(clojure.string/starts-with? ?status "${this.STATUS_ATTRIB}")]]`;
    return await window.roamAlphaAPI.q(activesprint_q);
  },
  async getTeam () {
    let team_q = `[:find ?team_member ?person_page
 				   :where [?page  :node/title "${this.TEAM_PAGE}"]
		                  [?block :block/page ?page]
		                  [?block :block/string ?team_member]
		                  [?block :block/refs ?person_page]]`;

	return await window.roamAlphaAPI.q(team_q);
  },
  async getSprintPlanKanbanStatusBlocks(UID) {
    let status_q = `[:find ?kstate_block ?kanban_status ?order
                     :where [?this_block       :block/uid      "${UID}"]
                            [?this_block       :block/page     ?this_page]
                            [?sprintplan_block :block/page     ?this_page]
                            [?sprintplan_block :block/string   ?string]			     
                            [(clojure.string/starts-with? ?string "${this.SPRINTPLAN_BLOCK}")]
                            [?kanban_block     :block/parents  ?sprintplan_block]
                            [?kanban_block     :block/string   "{{[[kanban]]}}"]
                            [?kanban_block     :block/children ?kstate_block]
                            [?kstate_block     :block/string   ?kanban_status]
                            [?kstate_block     :block/order    ?order]]`;

    return await window.roamAlphaAPI.q(status_q).sort((a, b) => a[2] - b[2]); //sort by order
  },
  async countStoryPoints(status_r) {
    let estimate_q = `[:find ?est ?title
                       :in $ ?kstate_block
                       :where [?kstate_block   :block/children ?story_block]
                              [?story_block    :block/refs     ?story_page]
                              [?story_page     :node/title     ?title]
                              [?estimate_block :block/page     ?story_page]
                              [?estimate_block :block/string   ?estimate]
                              [(clojure.string/starts-with? ?estimate "${this.ESTIMATE_ATTRIB}")]
                              [(subs ?estimate 10) ?est]]`;
    let story_points = [];
    for (let i=0;i<status_r.length;i++) {
      sum = await window.roamAlphaAPI.q(estimate_q,status_r[i][0])
                               .reduce((a,b) => a + parseInt(b[0]), 0);
      story_points.push([status_r[i][1],sum]);
    }
    return story_points;
  },
  async updateChart(sprint_title) {
    //This SB is currently hard coded to assume two data sets, "Done" 
    //and the Sum of all statuses before "Done".
    //"Done" is the last column of the kanban chart, the name can be different (e.g. "Complete")
    
   	let burndownuid_q = `
	   [:find ?uid
		:where [?sprint         :node/title "${sprint_title}"]
			   [?sprint         :block/children ?burndown_block]
			   [?burndown_block :block/string ?string]
		       [(clojure.string/starts-with? ?string "${this.BURNDOWN_BLOCK}")]
			   [?burndown_block :block/uid ?uid]]`;
    let UID = await window.roamAlphaAPI.q(burndownuid_q)[0][0];

	let status_r = await window.roamAgile.getSprintPlanKanbanStatusBlocks(UID);
   
    let story_points = await window.roamAgile.countStoryPoints(status_r);

    //find chart's lines (e.g. "To Do" and "Done")
    //note that the chart does not always include all statuses from the kanban board (.e.g missing "Doing")
    let chart_q = `[:find  ?cstate_block ?chart_status ?status_uid ?chart_uid
                    :where [?this_block   :block/uid      "${UID}"]
                           [?this_block   :block/page     ?this_page]		     
                           [?chart_block  :block/page     ?this_page]
                           [?chart_block  :block/string   "{{line}}"]
                           [?chart_block  :block/uid      ?chart_uid]
                           [?chart_block  :block/children ?cstate_block]
                           [?cstate_block :block/string   ?chart_status]
                           [?cstate_block :block/uid   ?status_uid]]`;

    let chart_r = await window.roamAlphaAPI.q(chart_q); 

    //count number of children for chart line
    let chartdata_q = `[:find ?block
                        :in $ ?status_block
                        :where [?status_block :block/children ?block]]`;

    //Currently hard coded, the burn down chart has two columns
    //all statuses except for the last "Done" are accumulated to the first column
    function getStoryPoints(s) {
      let i = 0;
      while (i<story_points.length) {
        if (story_points[i][0]==s) 
          if (i == story_points.length-1)
            return story_points[i][1]; //if this is the last, this is "Done", return the Done values
          else 
            //else sum up all the story points and substract "Done" points
            return story_points.reduce((a,b) => a + b[1], 0) - story_points[story_points.length-1][1];
        i += 1;
      }
      return 0;
    } 

    //add data points to the chart
    for (i=0;i<chart_r.length;i++) {
      num_datapoints = await window.roamAlphaAPI.q(chartdata_q,chart_r[i][0]).length; 
      await roam42.common.createBlock (chart_r[i][2],num_datapoints,(num_datapoints)+', '+getStoryPoints(chart_r[i][1]));
    }


    //This is an ugly workaround. I was not able to get the chart to update. The only solution I could find is to
    //replace the chart with an empty string and change it back after 500ms
    if (chart_r.length>0) {
      await roam42.common.updateBlock(chart_r[0][3]," ",false);
      await window.roamAgile.sleep(500);
      await roam42.common.updateBlock(chart_r[0][3],"{{line}}",false);
    }
  } 
}```
