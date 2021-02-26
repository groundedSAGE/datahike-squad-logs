- #42SmartBlock Standup <%NOCURSOR%>
    - <%JA:```javascript
const QUESTIONS = ['How are you feeling?',
                   'What did you accomplish since yesterday?',
                   'What will you work on today?',
                   'Do you need any help?'];

//get detailes on current block
let curblock_q = `[:find ?parentuid ?order
 :where [?block  :block/uid "${document.activeElement.id.slice(-9)}"]
        [?block  :block/order ?order]
		[?parent :block/children ?block]
		[?parent :block/uid ?parentuid]]`;

let curblock_r = await window.roamAlphaAPI.q(curblock_q);
let order = curblock_r[0][1]+1;
let parent = curblock_r[0][0];

//get active sprint
let activesprint_r = await window.roamAgile.getActiveSprint();

//Team members are the blocks on the [[Team]] page
let team_r = await window.roamAgile.getTeam();

//Developer stories
let activestory_q = `[:find ?story:name ?story:uid ?status ?sprint ?order
 :in $ ?person_block 
 :where [?story_page :node/title ?story:name]
		[?story_page :block/uid ?story:uid]
		[?story_page :block/children ?assign_block]
		[?story_page :block/children ?status_block]
        [(clojure.string/starts-with? ?story:name "${window.roamAgile.STORY_NAMESPACE}")]
		
		[?assign_block :block/string ?assign_string]
		[(clojure.string/starts-with? ?assign_string "${window.roamAgile.ASSIGNEDTO_ATTRIB}")]
        [?assign_block :block/refs ?person_block]

		[?status_block :block/string ?status_string]
		[(clojure.string/starts-with? ?status_string "${window.roamAgile.STATUS_ATTRIB+' #'+window.roamAgile.STATUS_ACTIVE}")]
		[?active_page :node/title "${window.roamAgile.STATUS_ACTIVE}"]
		[?status_block :block/refs ?active_page]
 
 		[?kanban :block/string "{{[[kanban]]}}"]
 		[?sprintplan :block/string ?sp_string]
 		[(clojure.string/starts-with? ?sp_string "${window.roamAgile.SPRINTPLAN_BLOCK}")]
        [?sprintplan :block/children ?kanban]
 		[?block  :block/refs ?story_page]
 		[?block  :block/parents ?kanban]
 		[?kanban :block/children ?state_block]
 		[?state_block :block/children ?block]
 		[?state_block :block/string ?status]
		[?state_block :block/order ?order]
        [?kanban :block/page ?page]
 		[?page :node/title ?sprint]]`;

for (i=0;i<team_r.length;i++) { 
  uid = await roam42.common.createBlock(parent,order,team_r[i][0]);
  order += 1;
  activestory_r = await window.roamAlphaAPI.q(activestory_q,team_r[i][1]).sort((a, b) => a[4]-b[4]);  
  uid2 = await roam42.common.createBlock(uid,0,"{{[[kanban]]}}");
  await roam42.common.updateBlock(uid2,"{{[[kanban]]}}",false); //workaround until 
  uid3 = '';
  story_state_order = 0;
  story_order = 0;
  story_state = '';
  if (activesprint_r.length>0) 
    for(k=0;k<activestory_r.length;k++) {
      if (activestory_r[k][3] == activesprint_r[0][0]) {
        if (story_state != activestory_r[k][2]) {
          story_state = activestory_r[k][2];
          uid3 = await roam42.common.createBlock(uid2,story_state_order,story_state);
          story_state_order += 1;
          story_order = 0;
        }
        await roam42.common.createBlock(uid3,k,'[['+activestory_r[k][0]+']]');
        story_order +=1;
      }
    }
    
  for (j=0;j<QUESTIONS.length;j++) {
    uid2 = await roam42.common.createBlock(uid,j+1,QUESTIONS[j]);
    await roam42.common.createBlock(uid2,0,' ');
  }
}

if (activesprint_r.length>0) {
  if (confirm("Do you want to update the Burn Down Chart for Current Sprint?"))
    window.roamAgile.updateChart(activesprint_r[0][0]);
  return '**Active Sprint:** [['+activesprint_r[0][0]+']]';
}
else
  return 'No sprint/ with #status/active found';```%>
