- #42SmartBlock Start Sprint <%HIDE%><%NOCURSOR%>
    - <%NOBLOCKOUTPUT%><%J:```javascript
uid = document.activeElement.id.slice(-9);
roam42.common.updateBlock(uid,window.roamAgile.STATUS_ATTRIB+' #'+window.roamAgile.STATUS_ACTIVE);
q = `[:find ?title
      :where [?block :block/uid "${uid}"]
			 [?block :block/page ?page]
			 [?page  :node/title ?title]]`;
window.roamAgile.updateChart(window.roamAlphaAPI.q(q)[0][0]);```%>
