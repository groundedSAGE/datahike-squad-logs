- #42SmartBlock Backlog Update <%NOCURSOR%><%HIDE%>
    - <%NOBLOCKOUTPUT%><%J:```javascript
const STORY   = window.roamAgile.STORY_NAMESPACE; 
const BACKLOG = window.roamAgile.BACKLOG_PAGE; 
let current_block_uid = document.activeElement.id.slice(-9);

let story_q = `[:find ?Story ?uid
   		        :where [?p :node/title ?Story]
					   [?p :block/uid ?uid]
		         	   [(clojure.string/starts-with? ?Story "${STORY}")]
		                (not-join [?p]
                  		[?back :node/title "${BACKLOG}"]
		          		[?bck  :block/page ?back]
		          		[?bck  :block/refs ?p])]`;

let last_story_q = `[:find (max ?order) 
					 :where [?b :block/uid "${current_block_uid}"]
							[?b :block/children ?c]
							[?c :block/order ?order]]`;
						
order = window.roamAlphaAPI.q(last_story_q);
order = (order.length>0) ? order[0][0]+1 : 0;

stories = window.roamAlphaAPI.q(story_q);

for (let i=0;i<stories.length;i++) {
  roam42.common.createBlock (current_block_uid,order,'{{[[TODO]]}} [['+stories[i][0]+']]');
  order += 1;
}```%>
