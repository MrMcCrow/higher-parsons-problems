---
layout: default
title: Page 2
---


<div id="findMax-sortableTrash" class="sortable-code"></div> 
<div id="findMax-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="findMax-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="findMax-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def findMax(my_array):\n" +
    "	max = my_array[0]\n" +
    "	for i in my_array:\n" +
    "		if i &gt; max:\n" +
    "			max = i\n" +
    "	return max\n" +
    "for i in range (len(my_array)): #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "findMax-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "findMax-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#findMax-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#findMax-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

[Previous](index.markdown)
[Next](./example2.html)
