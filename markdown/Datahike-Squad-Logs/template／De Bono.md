- [Zsolt.Blog: De Bono's Algorithms of Thought  for Lateral Thinking and Creativity Part 1](https://www.zsolt.blog/2020/12/de-bonos-algorithms-of-thought-for.html)
    - #42SmartBlock CAF - [[AoT/CAF: Consider All Factors]]
        - #CAF
            - **Situation:** <%JAVASCRIPT: situation=prompt('What situation are you facing?');roam42.smartBlocks.activeWorkflow.vars['situation']=situation; return situation;%>
            - **Factors to consider:**
                - <%J: ```javascript
factor1 = prompt('Tell me one factor that comes to mind when thinking about "' 
                 + roam42.smartBlocks.activeWorkflow.vars['situation'] + '"'); 
msg='Factors for "' + roam42.smartBlocks.activeWorkflow.vars['situation'] 
    + '":\n- ' + factor1 + '\n'; 
roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor1, false);

do { 
  factor = prompt(msg+'What else must be considered?\n(Empty Ok or Cancel to STOP)'); 
  if(factor!='' && !(factor === null)) { 
    roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor, false); 
    msg += '- '+factor+'\n'; 
  } 
} while (factor!='' && !(factor === null)); ```%>
    - #42SmartBlock APC - [[AoT/APC: Alternatives, Possibilities, Choices]]
        - #APC
            - **Situation:** <%JAVASCRIPT: situation=prompt('What situation are you facing?');roam42.smartBlocks.activeWorkflow.vars['situation']=situation; return situation;%>
            - **Alternatives, Possibilities, Choices:**
                - <%J: ```javascript
factor1 = prompt('Tell me one way to approach to "' 
                 + roam42.smartBlocks.activeWorkflow.vars['situation'] + '"'); 
msg='Alternatives, Possibilities and Choices for "' 
    + roam42.smartBlocks.activeWorkflow.vars['situation'] 
    + '":\n- ' + factor1 + '\n'; 
roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor1, false); 

do { 
  factor = prompt(msg+'What additional alternatives can you think of?\n(Empty Ok or Cancel to STOP)'); 
  if(factor!='' && !(factor === null)) { 
    roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor, false); 
    msg += '- '+factor+'\n'; 
  } 
} while (factor!='' && !(factor === null)); ```%>
    - #42SmartBlock OPV - [[AoT/OPV: Other People's Views]]
        - #OPV
            - **Situation:** <%JAVASCRIPT: situation=prompt('What situation are you facing?'); roam42.smartBlocks.activeWorkflow.vars['situation']=situation; return situation;%>
            - **Who are affected and what are their views?**
                - {{table}}
                    - <%NOBLOCKOUTPUT%><%JA:```javascript
function addPersonView(uid, person,order,views) {
  let uid2 = roam42.common.createUid();
  window.roamAlphaAPI.createBlock(
    {"location":{"parent-uid":uid,"order": order},"block":{"string":person,"uid":uid2}});
  window.roamAlphaAPI.createBlock(
    {"location":{"parent-uid":uid2,"order": 0},"block":{"string":views}});
}

let uid = document.querySelector("textarea.rm-block-input").id;
uid = uid.substring( uid.length -9);
addPersonView(uid,'**People or groups affected**',0,'**What views are they holding?**');
     
person1 = prompt('Tell me a person or group who is affected by "' 
                 + roam42.smartBlocks.activeWorkflow.vars['situation'] + '"');

msg='People or groups affected by "' + roam42.smartBlocks.activeWorkflow.vars['situation'] 
                                     + '":\n- ' + person1 + '\n'; 
var people = [person1];
do { 
     person = prompt(msg+'Name another person or group affected?\n(Empty Ok or Cancel to STOP)'); 
     if(person !='') { 
          people.push(person);
          msg += '- '+person+'\n'; 
     } 
} while (person!='');

for(var i=0; i < people.length; i++) {
  view1 = prompt('Put yourself in the shoes of ' + people[i] + '. How do you view the situation, what are you thinking?');
  msg='- ' + view1; 
  do { 
    view = prompt('Views and thoughts of ' + people[i] + ' are:\n'+msg+'\nAs ' + people[i] + ' what else are you thinking?\n(Empty Ok or Cancel to STOP)'); 
    if(view !='') { 
      msg += '\n- '+view; 
    } 
  } while (view!=''); 
  addPersonView(uid, people[i],i+1,msg);
}```
%>
    - #42SmartBlock CnS [[AoT/CnS: Consequence and Sequel]]
        - #CnS
            - **Situation:** <%CURSOR%>
                - What is the ideal, worst and most likely outcome?
                    - Immediately
                        -  
                    - Short-term
                        -  
                    - Medium-term
                        -  
                    - Long-term
                        -  
                - What are the benefits?
                    -  
                - What could be some problems or risks?
                    -  
                - What are the costs?
                    -  
                - How certain are you about your prediction as to what will happen?
                    - {{slider}}
    - #42SmartBlock PMI - [[AoT/PMI: Plus, Minus and Interesting]]
        - #PMI
            - **Case:** <%JAVASCRIPT: situation=prompt('What case/proposal are you facing?');roam42.smartBlocks.activeWorkflow.vars['situation']=situation; return situation;%>
            - **Plus:**
                - <%J: ```javascript
factor1 = prompt('Tell me one PLUS aspect that comes to mind when thinking about "' 
                 + roam42.smartBlocks.activeWorkflow.vars['situation'] + '"'); 
msg='Factors for "' 
     + roam42.smartBlocks.activeWorkflow.vars['situation'] 
     + '":\n- ' + factor1 + '\n';
roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor1, false);

do { 
  factor = prompt(msg+'What other PLUS aspects can you think of?\n(Empty Ok or Cancel to STOP)'); 
  if(factor!='' && !(factor === null)) { 
    roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor, false); 
    msg += '- '+factor+'\n'; 
  } 
} while (factor!='' && !(factor === null)); ``` %>
            - **Minus:**
                - <%J: ```javascript
factor1 = prompt('Tell me one MINUS aspect that comes to mind when thinking about "' 
                 + roam42.smartBlocks.activeWorkflow.vars['situation'] + '"'); 
msg='Factors for "' 
     + roam42.smartBlocks.activeWorkflow.vars['situation'] 
     + '":\n- ' + factor1 + '\n'; 
roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor1, false);

do { 
  factor = prompt(msg+'What other MINUS aspects can you think of?\n(Empty Ok or Cancel to STOP)'); 
  if(factor!='' && !(factor === null)) { 
    roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor, false); 
    msg += '- '+factor+'\n'; 
  } 
} while (factor!='' && !(factor === null)); ```%>
            - **Interesting:**
                - <%J: ```javascript
factor1 = prompt('Tell me one INTERESTING aspect that comes to mind when thinking about "' 
                 + roam42.smartBlocks.activeWorkflow.vars['situation'] + '"'); 

msg='Factors for "' 
    + roam42.smartBlocks.activeWorkflow.vars['situation'] 
    + '":\n- ' + factor1 + '\n'; 
roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor1, false); 

do { 
  factor = prompt(msg+'What other INTERESTING aspects can you think of?\n(Empty Ok or Cancel to STOP)'); 
  if(factor!='' && !(factor === null)) { 
    roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor, false); 
    msg += '- '+factor+'\n'; 
  } 
} while (factor!='' && !(factor === null)); ```%>
- [Zsolt.Blog: De Bono's Algorithms of Thought  for Handling Disagreements](https://www.zsolt.blog/2020/12/de-bonos-algorithms-of-thought-for_8.html)
    - #42SmartBlock ADI and EBS - [[AoT/ADI: Agreement, Disagreement and Irrelevance]], [[AoT/EBS: Examine Both Sides]]
        - #ADI
            - **Case:** <%J: ```javascript
situation=prompt('Consider the other\'s point of view in the disagreement or negotiation situation. What really is the other point of view? Remember to do your best to remain neutral in your assessment!');
roam42.smartBlocks.activeWorkflow.vars['situation']=situation; 
return situation;```%>
            - **Agreement:**
                - <%J: ```javascript
factor1 = prompt('What are you in agreement about regarding "' 
                 + roam42.smartBlocks.activeWorkflow.vars['situation'] + '"'); 
msg='Factors for "' + roam42.smartBlocks.activeWorkflow.vars['situation'] 
    + '":\n- ' + factor1 + '\n'; 
roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor1, false);

do { 
  factor = prompt(msg+'What other aspects do the two of you agree on?\n(Empty Ok or Cancel to STOP)');
  if(factor!='' && !(factor === null)) { 
    roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor, false); 
    msg += '- '+factor+'\n'; 
  } 
} while (factor!='' && !(factor === null)); ```%>
            - **Disagreement:**
                - <%J: ```javascript
factor1 = prompt('What are you in disagreement about regarding "' 
                 + roam42.smartBlocks.activeWorkflow.vars['situation'] + '"'); 
msg='Factors for "' + roam42.smartBlocks.activeWorkflow.vars['situation'] 
    + '":\n- ' + factor1 + '\n'; 
roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor1, false);

do { 
  factor = prompt(msg+'What other aspects do the two of you disagree on?\n(Empty Ok or Cancel to STOP)'); 
  if(factor!='' && !(factor === null)) { 
    roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor, false); 
    msg += '- '+factor+'\n'; 
  } 
} while (factor!='' && !(factor === null)); ```%>
            - **Irrelevance:**
                - <%J: ```javascript
factor1 = prompt('What are of irrelevance to you regarding "' 
                 + roam42.smartBlocks.activeWorkflow.vars['situation'] + '"'); 
msg='Factors for "' + roam42.smartBlocks.activeWorkflow.vars['situation'] 
    + '":\n- ' + factor1 + '\n'; 
roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor1, false);

do { 
  factor = prompt(msg+'What other aspects are of irrelevance?\n(Empty Ok or Cancel to STOP)'); 
  if(factor!='' && !(factor === null)) { 
    roam42.smartBlocks.activeWorkflow.outputAdditionalBlock(factor, false); 
    msg += '- '+factor+'\n'; 
  } 
} while (factor!='' && !(factor === null)); ```%>
