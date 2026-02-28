# You
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Drakon System</title>

<style>

body{
background:#000000;
color:#00ffe1;
font-family:Consolas,monospace;
text-align:center;
padding:20px;
}

/* SYSTEM BOOT TEXT */
.system{
font-size:30px;
font-weight:bold;
letter-spacing:4px;
margin-top:60px;
animation:glow 1.5s infinite alternate;
}

@keyframes glow{
from{opacity:.5;text-shadow:0 0 5px #00ffe1;}
to{opacity:1;text-shadow:0 0 20px #00ffe1;}
}

/* PANELS */
.panel{
display:none;
margin-top:35px;
padding:25px;
border:2px solid #00ffe1;
border-radius:12px;
box-shadow:0 0 25px #00ffe1;
background:#000;
animation:fade 0.8s ease;
}

@keyframes fade{
from{opacity:0;transform:translateY(15px);}
to{opacity:1;}
}

input{
padding:10px;
margin-top:10px;
background:black;
color:#00ffe1;
border:1px solid #00ffe1;
width:70%;
}

button{
margin-top:18px;
padding:10px 22px;
background:#00ffe1;
border:none;
font-weight:bold;
cursor:pointer;
border-radius:6px;
}

.reward{
text-align:left;
margin:auto;
width:260px;
line-height:2;
}

</style>
</head>

<body>

<!-- SYSTEM BOOT -->
<div id="boot" class="system">
SYSTEM INITIALIZING...
</div>


<!-- HOST -->
<div id="names" class="panel">
<h2>HOST DETECTED</h2>

<p>Emmanuel</p>
<p>Sunbola</p>
<p>Praise</p>

<p><b>ENTER PASSWORD</b></p>

<input id="password" type="password">
<br>

<button onclick="checkPassword()">ACCESS SYSTEM</button>

<p id="error"></p>
</div>


<!-- GREETING -->
<div id="greeting" class="panel">

<h2>SYSTEM MESSAGE</h2>

<p>
Today marks more than a birthday.<br><br>

May your life be filled with:<br><br>

✨ Joy<br>
✨ Success<br>
✨ Happiness<br>
✨ Growth<br>
✨ Fulfilled Dreams<br><br>

Emmanuel.<br>
Sunbola.<br>
Praise.<br><br>

You shall soon live the life you desire.<br><br>

Happy Birthday, Drakon.
</p>

<button onclick="showReward()">ACCEPT REWARD</button>

</div>


<!-- SECRET -->
<div id="secret" class="panel">

<h3>SECRET AUTHENTICATION</h3>

<p>Input Secret Code (D)</p>

<input id="code">
<br>

<button onclick="unlockReward()">UNLOCK</button>

</div>


<!-- FINAL REWARD -->
<div id="finalReward" class="panel">

<h2>✅ SYSTEM STATUS</h2>

<div class="reward">

Name: <b>Drakon</b><br>
Race: Human<br><br>

Perks Added:<br>

💰 Wealth +100<br>
❤️ Health +100<br>
😊 Happiness +100

</div>

<br>

<button onclick="playMusic()">INITIATE CELEBRATION</button>

</div>


<!-- MUSIC -->
<iframe id="music"
width="0"
height="0"
allow="autoplay">
</iframe>


<script>

/* SYSTEM BOOT */
setTimeout(()=>{
document.getElementById("boot").style.display="none";
document.getElementById("names").style.display="block";
},3000);


/* PASSWORD */
function checkPassword(){

let pass=document.getElementById("password").value;

if(pass==="Drakon" || pass==="drakon"){
document.getElementById("names").style.display="none";
document.getElementById("greeting").style.display="block";
}else{
document.getElementById("error").innerText="ACCESS DENIED";
}
}


/* SHOW SECRET */
function showReward(){
document.getElementById("greeting").style.display="none";
document.getElementById("secret").style.display="block";
}


/* UNLOCK REWARD */
function unlockReward(){

let code=document.getElementById("code").value;

if(code==="D" || code==="d"){
document.getElementById("secret").style.display="none";
document.getElementById("finalReward").style.display="block";
}else{
alert("INVALID CODE");
}
}


/* MUSIC */
function playMusic(){
document.getElementById("music").src=
"https://www.youtube.com/embed/WcIcVapfqXw?autoplay=1";
}

</script>

</body>
</html>
