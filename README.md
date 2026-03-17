```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Doraemon Movie 💙</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>

body{
margin:0;
background:black;
color:white;
font-family:Arial;
overflow:hidden;
text-align:center;
}

/* scenes */

.scene{
position:absolute;
width:100%;
height:100vh;
display:flex;
justify-content:center;
align-items:center;
flex-direction:column;
opacity:0;
transition:opacity 1.5s;
}

.active{
opacity:1;
}

video{
position:absolute;
width:100%;
height:100%;
object-fit:cover;
z-index:-1;
}

.overlay{
position:absolute;
width:100%;
height:100%;
background:rgba(0,0,0,0.5);
z-index:-1;
}

.text{
font-size:28px;
max-width:600px;
padding:20px;
animation:fade 2s;
}

@keyframes fade{
from{opacity:0; transform:translateY(40px);}
to{opacity:1;}
}

button{
padding:12px 25px;
background:#0072ff;
border:none;
border-radius:25px;
color:white;
font-size:18px;
margin-top:20px;
cursor:pointer;
}

</style>
</head>

<body>

<!-- VOICE -->
<audio autoplay>
<source src="voice.mp3">
</audio>

<!-- SCENE 1 -->

<div class="scene active" id="s1">

<video autoplay muted loop>
<source src="scene1.mp4">
</video>

<div class="overlay"></div>

<div class="text">
🎬 Ek kahani... Adesh aur Rupashree ki ❤️
</div>

<button onclick="next('s2')">▶</button>

</div>

<!-- SCENE 2 -->

<div class="scene" id="s2">

<video autoplay muted loop>
<source src="scene2.mp4">
</video>

<div class="overlay"></div>

<div class="text">
👦 Adesh... ek Nobita jaisa ladka 😅  
Thoda annoying... par dil se accha ❤️
</div>

<button onclick="next('s3')">▶</button>

</div>

<!-- SCENE 3 -->

<div class="scene" id="s3">

<video autoplay muted loop>
<source src="scene3.mp4">
</video>

<div class="overlay"></div>

<div class="text">
👧 Rupashree... uski Shizuka 💙  
Jiske bina sab adhura hai 🥺
</div>

<button onclick="next('s4')">▶</button>

</div>

<!-- SCENE 4 -->

<div class="scene" id="s4">

<video autoplay muted loop>
<source src="scene4.mp4">
</video>

<div class="overlay"></div>

<div class="text">
💔 Kabhi kabhi galti ho jati hai...  
Aur wo usse hurt kar deta hai 😔
</div>

<button onclick="next('s5')">▶</button>

</div>

<!-- SCENE 5 -->

<div class="scene" id="s5">

<video autoplay muted loop>
<source src="scene5.mp4">
</video>

<div class="overlay"></div>

<div class="text">
💌 Par sach ye hai...  
Wo usse bahut pyaar karta hai ❤️  
Aur usse khona nahi chahta 🥺
</div>

<button onclick="next('final')">▶</button>

</div>

<!-- FINAL -->

<div class="scene" id="final">

<video autoplay muted loop>
<source src="scene6.mp4">
</video>

<div class="overlay"></div>

<div class="text">
💍 Kya tum mujhe maaf karogi? 🥺  
Main better banunga... pakka ❤️
</div>

<button onclick="alert('I love you ❤️')">💙 Yes</button>

</div>

<script>

function next(id){

document.querySelectorAll(".scene").forEach(s=>{
s.classList.remove("active")
})

document.getElementById(id).classList.add("active")

}

</script>

</body>
</html>
```
index.html
scene1.mp4
scene2.mp4
scene3.mp4
scene4.mp4
scene5.mp4
scene6.mp4
voice.mp3
