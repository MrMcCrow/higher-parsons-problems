---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Higher Parson's Problems
---
# Parsons Practice

## Standard Algorithms - findMax - Python
Re-arrange the blocks below

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



[Next](./parsons/example1.html)
