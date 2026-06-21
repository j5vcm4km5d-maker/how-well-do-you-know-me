<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>How Well Do You Know Me?</title>

<style>
body{
    font-family: Arial, sans-serif;
    background: linear-gradient(135deg,#111,#333);
    color:white;
    text-align:center;
    padding:20px;
}

.container{
    max-width:700px;
    margin:auto;
    background:#222;
    padding:20px;
    border-radius:20px;
}

.question{
    margin:25px 0;
}

button{
    background:black;
    color:white;
    border:none;
    padding:12px 25px;
    border-radius:10px;
    cursor:pointer;
    font-size:16px;
}

button:hover{
    opacity:0.8;
}

.result{
    font-size:28px;
    margin-top:20px;
}
</style>
</head>
<body>

<div class="container">
<h1>😎 How Well Do You Know Me?</h1>

<form id="quizForm">

<div class="question">
<h3>1. What is my favorite color?</h3>
<label><input type="radio" name="q1" value="Black"> Black</label><br>
<label><input type="radio" name="q1" value="Blue"> Blue</label><br>
<label><input type="radio" name="q1" value="Red"> Red</label>
</div>

<div class="question">
<h3>2. How many hours do I sleep?</h3>
<label><input type="radio" name="q2" value="9"> 9 Hours</label><br>
<label><input type="radio" name="q2" value="6"> 6 Hours</label><br>
<label><input type="radio" name="q2" value="12"> 12 Hours</label>
</div>

<div class="question">
<h3>3. How tall am I?</h3>
<label><input type="radio" name="q3" value="6'1"> 6'1</label><br>
<label><input type="radio" name="q3" value="5'9"> 5'9</label><br>
<label><input type="radio" name="q3" value="6'5"> 6'5</label>
</div>

<div class="question">
<h3>4. What is my weight?</h3>
<label><input type="radio" name="q4" value="76"> 76 kg</label><br>
<label><input type="radio" name="q4" value="68"> 68 kg</label><br>
<label><input type="radio" name="q4" value="82"> 82 kg</label>
</div>

<div class="question">
<h3>5. Who is most important to me?</h3>
<label><input type="radio" name="q5" value="Mum"> Mum ❤️</label><br>
<label><input type="radio" name="q5" value="Friends"> Friends</label><br>
<label><input type="radio" name="q5" value="Teacher"> Teacher</label>
</div>

<div class="question">
<h3>6. What is my favorite subject?</h3>
<label><input type="radio" name="q6" value="English"> English</label><br>
<label><input type="radio" name="q6" value="Math"> Math</label><br>
<label><input type="radio" name="q6" value="Science"> Science</label>
</div>

<button type="button" onclick="checkQuiz()">Submit</button>

</form>

<div class="result" id="result"></div>

</div>

<script>
function checkQuiz(){

let score = 0;

if(document.querySelector('input[name="q1"]:checked')?.value==="Black") score++;
if(document.querySelector('input[name="q2"]:checked')?.value==="9") score++;
if(document.querySelector('input[name="q3"]:checked')?.value==="6'1") score++;
if(document.querySelector('input[name="q4"]:checked')?.value==="76") score++;
if(document.querySelector('input[name="q5"]:checked')?.value==="Mum") score++;
if(document.querySelector('input[name="q6"]:checked')?.value==="English") score++;

const result = document.getElementById("result");

if(score === 6){
    result.innerHTML =
    "🏆 PERFECT! You know me extremely well! 😎";
}
else if(score >= 4){
    result.innerHTML =
    "🎉 Great Job! Score: " + score + "/6";
}
else{
    result.innerHTML =
    "😅 Score: " + score + "/6. Try again!";
}
}
</script>

</body>
</html>