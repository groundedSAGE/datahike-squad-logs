- #42SmartBlock Count Story Points <%NOCURSOR%><%HIDE%>
    - <%NOBLOCKOUTPUT%><%JA:```javascript
const SPRINT_PLAN_BLOCK = "Sprint Plan"
let UID = document.activeElement.id.slice(-9);
let status_r = await window.roamAgile.getSprintPlanKanbanStatusBlocks(UID);
let story_points = await window.roamAgile.countStoryPoints(status_r);
window.datomicQuery.clearPrevious();
window.datomicQuery.processResults(story_points,'[:find ?Status ?Total :when');```%>
- ### #42SmartBlock Add Story Points to Chart <%NOCURSOR%><%HIDE%>
    - <%NOBLOCKOUTPUT%><%JA:```javascript
let UID = document.activeElement.id.slice(-9);
q = `[:find ?title
      :where [?block :block/uid "${UID}"]
			 [?block :block/page ?page]
			 [?page  :node/title ?title]]`;
window.roamAgile.updateChart(window.roamAlphaAPI.q(q)[0][0]);```%>
- 
