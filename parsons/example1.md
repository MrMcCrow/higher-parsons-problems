---
layout: default
title: Page 2
---


<div id="Input Validation - Pseudocode-sortableTrash" class="sortable-code"></div> 
<div id="Input Validation - Pseudocode-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Input Validation - Pseudocode-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Input Validation - Pseudocode-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "RECEIVE input FROM KEYBOARD\n" +
    "WHILE input &lt; min OR input &gt; max DO\n" +
    "	SEND error_message TO DISPLAY\n" +
    "	RECEIVE input FROM KEYBOARD\n" +
    "END WHILE\n" +
    "FOR i IN RANGE(LENGTH(input)) #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Input Validation - Pseudocode-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "Input Validation - Pseudocode-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Input Validation - Pseudocode-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Input Validation - Pseudocode-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

[Next](./example2.html)
