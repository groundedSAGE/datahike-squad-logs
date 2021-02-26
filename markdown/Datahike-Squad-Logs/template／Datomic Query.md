- # Query execution
    - #42SmartBlock Datomic simple-query <%NOCURSOR%><%HIDE%>
        - <%NOBLOCKOUTPUT%><%J:```javascript
let reg_parent_string = new RegExp('\`\`\`clojure\\s(.+)\`\`\`','s');

window.datomicQuery.overwriteBlockUID = null;
if (roam42.smartBlocks.activeWorkflow.vars['clearPrevious'] == 'true') 
  	window.datomicQuery.clearPrevious();

let query;
try{
  query = window.datomicQuery.getParentBlock()[0][0].match(reg_parent_string)[1];
} catch (err) {
  window.datomicQuery.writeBlock('ERROR - make sure you run the query from a block nested immediately under your query. Also check that common functions on [[Template/Datomic Query]] are running.');
  return null;
}

//Execute query
let results;
try { 	
  results = window.roamAlphaAPI.q(query);
} catch (err) {
  window.datomicQuery.writeBlock(err.toString());
  return null;
}

window.datomicQuery.processResults(results,query);
//return window.datomicQuery.processResults(results,query) + ']]]';```%>
    - #42SmartBlock Datomic advanced-query <%NOCURSOR%><%HIDE%>
        - <%NOBLOCKOUTPUT%><%J:```javascript
let reg_parent_string = new RegExp('\`\`\`javascript\\s(.+)\`\`\`','s');
let script_to_run;

window.datomicQuery.overwriteBlockUID = null;
if (roam42.smartBlocks.activeWorkflow.vars['clearPrevious']=='true') 
  	window.datomicQuery.clearPrevious();

try {
  script_to_run = window.datomicQuery.getParentBlock()[0][0].match(reg_parent_string)[1];
} catch (err) {
  window.datomicQuery.writeBlock('ERROR - make sure you run the query from a block nested immediately under your query. Also check that common functions on [[Template/Datomic Query]] are running.');
  return null;
}

//Execute query
let res;
try {
  res = new Function(script_to_run.toString())();
} catch (err) {
  window.datomicQuery.writeBlock(err.toString());
  return null;
}
let query = res[0];
let results = res[1];

window.datomicQuery.processResults(results,query);
//return window.datomicQuery.processResults(results,query) + ']]]';```%>
- # Templates
    - #42SmartBlock Datomic simple-template <%NOCURSOR%>
        - <%J:```javascript
let s = "\`\`\`clojure\n";
s += '[:find ?title:name ?title:uid ?time:date\n';
s += ' :where [?page :node/title ?title:name]\n';
s += '        [?page :block/uid ?title:uid]\n';
s += '        [?page :edit/time ?time:date]\n';
s += '        [(clojure.string/starts-with? ?title:name "roam/")]]';
s += "\`\`\`";
return s;```%>
            - {{UPDATE RESULTS:42SmartBlock:Datomic simple-query:clearPrevious=true,42RemoveButton=false}}
    - #42SmartBlock Datomic advanced-template <%NOCURSOR%>
        - <%J:```javascript
let s = "\`\`\`javascript\n";
s += "window.datomicQuery.MAXROWS = 40;\n\n";
s += "let rule = \`\`;\n\n";
s += "let query = `[:find ?title:name ?title:uid ?time:date\n";
s += "				:in $ ?namespace\n";
s += "				:where [?page :node/title ?title:name]\n";
s += "					   [?page :block/uid ?title:uid]\n";
s += "					   [?page :edit/time ?time:date]\n";
s += "					   [(clojure.string/starts-with? ?title:name ?namespace)]]`;\n\n";
s += "let results = window.roamAlphaAPI.q(query,'roam/');\n\n";
s += "return [query, results];";
s += "\`\`\`";
return s;```%>
            - {{UPDATE RESULTS:42SmartBlock:Datomic advanced-query:clearPrevious=true,42RemoveButton=false}}
    - #42SmartBlock Remove query-template header <%NOCURSOR%> <%HIDE%>
        - <%J:```javascript
let txt = document.querySelector("textarea.rm-block-input").value;
txt = txt.substr(txt.indexOf('`'));
document.querySelector("textarea.rm-block-input").value = '';
return txt;```%>
