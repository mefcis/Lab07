# Lab07

<html>
<body>

<p>I just created a simple math equation. Can you solve it?</p>

<p id="first"></p>
*
<p id="second"></p>
<input type="text" id="answerInput" > <br />

<button type="button" onclick="handleAnswer();">Answer</button>

<p>Now you edit one and try to solve it.</p>

<select onchange="myFunction(this)">
<option value = "num4">1</option>
<option value = "num4">2</option>
<option value = "num4">3</option>
<option value = "num4">4</option>
<option value = "num4">5</option>
<option value = "num4">6</option>
<option value = "num4">7</option>
<option value = "num4">8</option>
<option value = "num4">9</option>
<option value = "num4">10</option>
</select>

<br>

*

<p id="third"></p>

<br>

<input type="text" id="costomAnswerInput" > <br />

<button type="button" onclick="costomHandleAnswer();">Answer</button>

<script>
var num1 = Math.floor(Math.random() * 10) + 1  ;
var num2 = Math.floor(Math.random() * 10) + 1  ;
document.getElementById("first").innerHTML = num1;
document.getElementById("second").innerHTML = num2;

var handleAnswer = function(num) {
    var stringAnswer = document.getElementById('answerInput').value;
    
    var guess = parseInt(stringAnswer,10);
    
    if(guess == num1 * num2)
    {
        alert("You answered correctly!");
    }
    else
    {
        alert("Your answer is wrong. Try again.");
    }
};


var num3 = Math.floor(Math.random() * 10) + 1  ;
document.getElementById("third").innerHTML = num3;


function myFunction(selTag) {
    var num4 = selTag.options[selTag.selectedIndex].text;
	document.getElementById("forth").innerHTML = num4;
}

var costomHandleAnswer = function(num) {
    var costomAnswer = document.getElementById('costomAnswerInput').value;
    
    var cosAns = parseInt(costomAnswer);
    
    if(cosAns == num3 * num4)
    {
        alert("You answered correctly!");
    }
    else
    {
        alert("Your answer is wrong. Try again.");
    }
};

</script>
</body>
</html>
