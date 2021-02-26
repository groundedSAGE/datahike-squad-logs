- #42SmartBlock Close Sprint <%HIDE%><%NOCURSOR%>
    - <%NOBLOCKOUTPUT%><%J:```javascript
uid = document.activeElement.id.slice(-9);

let sprintstories_q = `
 [:find ?story_name ?story_page ?this_page ?sprint_name
  :where [?this_block       :block/uid      "${uid}"]
         [?this_block       :block/page     ?this_page]
         [?this_page        :node/title     ?sprint_name]
         [?sprintplan_block :block/page     ?this_page]
         [?sprintplan_block :block/string   ?string]
         [(clojure.string/starts-with? ?string "${window.roamAgile.SPRINTPLAN_BLOCK}")]
         [?sprintplan_block :block/children ?kanban_block]
         [?kanban_block     :block/string   ?kanban_string]
         [(= ?kanban_string "{{[[kanban]]}}")]
         [?story_block      :block/parents ?kanban_block]
         [?story_block      :block/refs ?story_page]
         [?story_page       :node/title ?story_name]]`;
let sprintstories_r = window.roamAlphaAPI.q(sprintstories_q);

let backlog_q = `
 [:find ?storyblock_uid ?sprintblock_uid
  :in $, ?story_block, ?sprint_page
  :where [?backlog_page      :node/title    "${window.roamAgile.BACKLOG_PAGE}"]
         [?sprintblock_block :block/page    ?backlog_page]
         [?sprintblock_block :block/refs    ?sprint_page]
		 [?sprintblock_block :block/uid     ?sprintblock_uid]
		 [?storyblock_block  :block/parents ?sprintblock_block]
         [?storyblock_block  :block/refs    ?story_block]
		 [?storyblock_block  :block/uid     ?storyblock_uid]]`;

let storystatus_q = `
 [:find ?statusblock_uid
  :in $, ?story_block
  :where [?status_block :block/page   ?story_block]
		 [?status_block :block/uid    ?statusblock_uid]
		 [?status_block :block/string ?status_string]
         [(clojure.string/starts-with? ?status_string "${window.roamAgile.STATUS_ATTRIB}")]]`;

let sprintstatus_q = `
 [:find ?statusblock_uid
  :in $, ?sprint_page
  :where [?status_block :block/page ?sprint_page]
         [?status_block :block/string ?status_string]
         [(clojure.string/starts-with? ?status_string "${window.roamAgile.STATUS_ATTRIB}")]
	     [?status_block :block/uid ?statusblock_uid]]`;

for (i=0;i<sprintstories_r.length;i++) {
  story_title      = sprintstories_r[i][0];
  storypage_entity = sprintstories_r[i][1];
  sprintpage_entity= sprintstories_r[i][2]; 
  if(confirm('Can I change status to closed for\n'+story_title)) {
    storystatus_r = window.roamAlphaAPI.q(storystatus_q,storypage_entity);
    backlog_r = window.roamAlphaAPI.q(backlog_q,storypage_entity,sprintpage_entity);

    if(storystatus_r.length==1) 
      roam42.common.updateBlock(storystatus_r[0][0],window.roamAgile.STATUS_ATTRIB+' #'+window.roamAgile.STATUS_CLOSED);
    else 
      alert('Something went wrong with setting status to "closed" for '+story_title);

    if(backlog_r.length ==1)
      roam42.common.updateBlock(backlog_r[0][0],'{{[[DONE]]}} [[' + story_title + ']]');
    else
      alert('Something went wrong with setting status to "closed" on backlog for '+story_title);
  }
}

if(sprintstories_r.length > 0)
  storypage_entity = sprintstories_r[0][1];
  sprintpage_entity= sprintstories_r[0][2];
  sprint_title     = sprintstories_r[0][3];
  if (confirm("Do you want to update the Burn Down Chart for Current Sprint?"))
    window.roamAgile.updateChart(sprint_title);  
  if(confirm('Can I set status of this sprint to closed?')) {
    sprintstatus_r = window.roamAlphaAPI.q(sprintstatus_q,sprintpage_entity);
    backlog_r = window.roamAlphaAPI.q(backlog_q,storypage_entity,sprintpage_entity);
    if(sprintstatus_r.length == 1) 
      roam42.common.updateBlock(sprintstatus_r[0][0],window.roamAgile.STATUS_ATTRIB+' #'+window.roamAgile.STATUS_CLOSED);
    else 
      alert ('Something went wrong with setting the status of this sprint to closed.');
    if(backlog_r.length > 0) 
      roam42.common.updateBlock(backlog_r[0][1],'{{[[DONE]]}} [[' + sprint_title + ']]');
    else
      alert ('Something went wrong with closing the sprint on the Backlog.');
  }```%>
