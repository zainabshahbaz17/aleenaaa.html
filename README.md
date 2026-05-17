<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Aleena 💖</title>

<style>

body{
margin:0;
font-family:Arial;
background:linear-gradient(135deg,#ffd6e8,#ffffff);
overflow:hidden;
}

.page{
width:100%;
height:100vh;
position:absolute;
top:0;
left:100%;
display:flex;
justify-content:center;
align-items:center;
transition:1s;
}

.active{
left:0;
}

.box{
width:80%;
padding:30px;
background:white;
border-radius:25px;
text-align:center;
box-shadow:0 0 20px pink;
}

h1{
color:#ff4d94;
}

button{
padding:14px 25px;
border:none;
border-radius:30px;
background:#ff4d94;
color:white;
cursor:pointer;
margin-top:20px;
}

.gallery img{
width:150px;
height:200px;
border-radius:15px;
margin:10px;
object-fit:cover;
}

.note{
padding:15px;
margin:10px;
background:#ffe6f0;
border-radius:20px;
}

.gift{
font-size:90px;
cursor:pointer;
animation:jump 1s infinite;
}

@keyframes jump{
50%{
transform:translateY(-10px);
}
}

.popup{
display:none;
position:fixed;
width:100%;
height:100%;
background:rgba(0,0,0,.5);
justify-content:center;
align-items:center;
}

.popupBox{
background:white;
padding:30px;
border-radius:20px;
text-align:center;
}

</style>
</head>

<body>

<div class="page active" id="page1">

<div class="box">
<h1>💖 Hi Aleena 💖</h1>

<p>You make every moment special ✨</p>

<button onclick="nextPage('page2')">
Open Memories 🌸
</button>

</div>

</div>

<div class="page" id="page2">

<div class="box">

<h1>💗 Our Memories 💗</h1>

<div class="gallery">

<img src="pic.jpg">
<img src="pg.jpg">
<img src="image.jpg">

</div>

<button onclick="nextPage('page3')">
Love Notes 💌
</button>

</div>

</div>

<div class="page" id="page3">

<div class="box">

<h1>💕 Cute Notes 💕</h1>

<div class="note">
Aleena you're amazing ❤️
</div>

<div class="note">
Thank you for always being there ✨
</div>

<div class="note">
Forever memories 💖
</div>

<button onclick="nextPage('page4')">
Open Gift 🎁
</button>

</div>

</div>

<div class="page" id="page4">

<div class="box">

<h1>Special Gift 💝</h1>

<div class="gift" onclick="gift()">
🎁
</div>

</div>

</div>

<div class="popup" id="popup">

<div class="popupBox">

<h2>💖</h2>

<h3>
Aleena, will you be my best friend forever?
</h3>

<button onclick="yes()">
Yes 💕
</button>

<button onclick="no()">
No 😒
</button>

<p id="answer"></p>

</div>

</div>

<script>

function nextPage(next){

let pages=document.querySelectorAll(".page");

pages.forEach(page=>{
page.classList.remove("active");
});

document.getElementById(next)
.classList.add("active");

}

function gift(){
document.getElementById("popup")
.style.display="flex";
}

function yes(){
document.getElementById("answer")
.innerHTML="Yayyyy 💖 Forever Best Friends";
}

function no(){
document.getElementById("answer")
.innerHTML="No option accepted 😂";
}

</script>

</body>
</html>
