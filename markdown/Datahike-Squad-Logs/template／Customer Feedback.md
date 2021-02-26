- This is now an extremely rudimentary implementation of a feedback import tool. Needs further work.
- Customer Feedback<%HIDE%><%NOCURSOR%>#42SmartBlock
    - 
    - {{[[TODO]]}} <%DATE: Today%> <%JA: ```javascript
let feedback = prompt('Please paste feedback here');
let sentiment = window.SentimentAnalysis.analyze(feedback);
let sentiment_text = '#sentiment/Neutral';
if ((sentiment<=1) && (sentiment>=-1))
  sentiment_text = '#sentiment/Neutral';
else if ((sentiment<-1) && (sentiment >= -4))
  sentiment_text = '#sentiment/Negative';
else if (sentiment<-4) 
  sentiment_text = '#sentiment/VeryNegative';
else if ((sentiment>1) && (sentiment<=4))
  sentiment_text = '#sentiment/Positive';
else 
  sentiment_text = '#sentiment/VeryPositive';

let feedbackType = prompt('Please select the feedback type\n1 - Feature request\n2 - General comment\n3 - Question\n\n'+feedback,2);
feedbackType_text = ' #feedbacktype/Comment'
switch (feedbackType) {
  case '1': feedbackType_text = ' #feedbacktype/Feature'; break;
  case '3': feedbackType_text = ' #feedbacktype/Question'; break;
  
}

team = await window.roamAgile.getTeam();
owner = ' {{Set Owner:42SmartBlock:Set Owner}}';
if (team.length>0) {
  o = prompt('Do you want to assign it now\n(leave empty if not, else type the number)?'
                 +team.reduce((res, val, ind) => res + '\n'+ind.toString()+': '+val[0], ''));
  owner = (o!='') ? ' '+team[o][0] : owner;
}
return sentiment_text + feedbackType_text + owner + '\n'+feedback;```%>
- Set Owner<%HIDE%><%NOCURSOR%>#42SmartBlock
    - <%JA: ```javascript
team = await window.roamAgile.getTeam();
owner = '';
if (team.length>0) {
  o = prompt('Enter number for owner or\nleave empty if you don\'t want to set an owner'
                 +team.reduce((res, val, ind) => res + '\n'+ind.toString()+': '+val[0], ''));
  owner = (o!='') ? ' '+team[o][0] : owner;
}
return owner;```%>
