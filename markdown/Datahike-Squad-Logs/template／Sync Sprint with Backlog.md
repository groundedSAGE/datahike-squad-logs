- #42SmartBlock Sync Sprint with Backlog <%NOCURSOR%><%HIDE%>
    - <%NOBLOCKOUTPUT%><%JA:```javascript

//const SPRINT_PLAN_BLOCK = "Sprint Plan"
let sprintplan = document.activeElement.id.slice(-9);

//stories already in the sprint
let sprintstories_q = `[:find ?story_block ?story_title ?block_uid
			            :where [?sprintplan :block/uid "${sprintplan}"]
					           [?block      :block/parents ?sprintplan]
					           [?block      :block/string  ?string]
					           [(clojure.string/includes?  ?string "${window.roamAgile.STORY_NAMESPACE}")]
					           [?block      :block/refs    ?story_block]
							   [?block      :block/uid     ?block_uid]
							   [?story_block :node/title   ?story_title]]`;

let sprintstories_r = window.roamAlphaAPI.q(sprintstories_q).sort((a, b) => a[0] - b[0]);

//stories on the backlog listed under this sprint
let backlogstories_q = `[:find ?story_block ?story_title
			            :where [?sprintplan  :block/uid     "${sprintplan}"]
					           [?sprintplan  :block/page    ?sprintpage]
							   [?sprint_ref  :block/refs    ?sprintpage]
							   [?backlog     :node/title    "${window.roamAgile.BACKLOG_PAGE}"]
					           [?sprint_ref  :block/page    ?backlog]
							   [?block       :block/parents ?sprint_ref]
					           [?block       :block/refs    ?story_block]
					           [?story_block :node/title    ?story_title]
					           [(clojure.string/includes?   ?story_title "${window.roamAgile.STORY_NAMESPACE}")]]`;

let backlogstories_r = window.roamAlphaAPI.q(backlogstories_q).sort((a, b) => a[0] - b[0]);

//next child order under first kanban column
let ktodochildren_q = `[:find ?stories
				        :where [?sprintplan :block/uid     "${sprintplan}"]
					           [?kanban     :block/parents ?sprintplan]
					           [?kanban     :block/string "{{[[kanban]]}}"]
					           [?kanban     :block/children ?cols]
       				           [?cols       :block/order ?o]
		       			       [(= ?o 0)]
				       	       [?cols       :block/children ?stories]]`

let ktodochildren_order = window.roamAlphaAPI.q(ktodochildren_q).length;

//get uid of first kanban column
let ktodouid_q = `[:find ?uid
				   :where [?sprintplan :block/uid     "${sprintplan}"]
					      [?kanban     :block/parents ?sprintplan]
					      [?kanban     :block/string "{{[[kanban]]}}"]
					      [?kanban     :block/children ?cols]
       				      [?cols       :block/order ?o]
		       		      [(= ?o 0)]
						  [?cols       :block/uid ?uid]]`

let ktodouid = window.roamAlphaAPI.q(ktodouid_q)[0][0];

let storystatus_q = `[:find ?uid
					 :in $ ?story_block
					 :where [?b :block/page ?story_block]
						    [?b :block/string ?string]
							[(clojure.string/starts-with?   ?string "${window.roamAgile.STATUS_ATTRIB}")]
						    [?b :block/refs ?refs]
							[?refs :node/title ?ref_string]
							[(= ?ref_string "${window.roamAgile.STATUS_DRAFT}")]
							[?b :block/uid ?uid]]`;

//add stories on backlog but not on sprint plan under todo
//set draft stories to active
for (let i=0;i<backlogstories_r.length;i++) {
  await window.roamAlphaAPI.q(storystatus_q,backlogstories_r[i][0])
    	.forEach(async function(element){ await roam42.common.updateBlock(element[0],'Status:: #'+window.roamAgile.STATUS_ACTIVE);});
  if (!sprintstories_r.some(row => row.includes(backlogstories_r[i][0]))) {
    await roam42.common.createBlock(ktodouid,ktodochildren_order,'[['+backlogstories_r[i][1]+']]');
    ktodochildren_order += 1;
  }
}

//remove stories from sprint plan that are not on the backlog
for (let i=0;i<sprintstories_r.length;i++) {
  if (!backlogstories_r.some(row => row.includes(sprintstories_r[i][0]))) 
    await roam42.common.deleteBlock(sprintstories_r[i][2]);
}```%>
- 
