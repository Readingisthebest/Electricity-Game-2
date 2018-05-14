# Electricity-Game-2
<!DOCTYPE html>
<html>  
<head>
<script>


function validateForm() {
	
    var name = document.forms["myForm"]["fname"].value;
    if (name == "") {
        alert("Name must be filled out");

    } else {
    	alert ("name is " + name); 
    	//ask_a_question("do you want to take the electricity quiz?","y");
    }
   
    return false;

}




function ask_a_question( q, a ){
	document.getElementById('quizquestions').innerHTML = q;
}

function checkQuizQuestion(){
	ask_a_question("do you turn off the tap while brushing your teeth?","y");
	var answer = document.forms["quizForm"]["quizAnswer"].value;
   	if (answer == "") {
        alert("Answer must be filled out");
 
    } else {
    	alert ("your answer is " + answer);
    } 
    return false;
}

</script>
</head>

<body>

<form name="myForm"  onsubmit="return validateForm()" method="get">
Name: <input type="text" name="fname">
<input type="submit" value="Submit">
</form>

<h3>Here is a quiz question</h3>
<p id="quizquestions"></p>
<h3>Enter an answer</h3>
<form name="quizForm"  onsubmit="return checkQuizQuestion()" method="get">
answer: <input type="text" name="quizAnswer">
<input type="submit" value="Submit">
</form>

</body>
</html>
