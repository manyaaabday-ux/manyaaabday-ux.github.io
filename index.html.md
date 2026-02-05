<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>Happy Birthday Manyaaa</title>  
  
<style>  
body {  
  margin: 0;  
  font-family: Arial, sans-serif;  
  background: #ffd6e0;  
  color: #7a1c3b;  
  text-align: center;  
}  
  
.screen {  
  min-height: 100vh;  
  display: none;  
  flex-direction: column;  
  justify-content: center;  
  align-items: center;  
  padding: 25px;  
}  
  
.screen.active {  
  display: flex;  
}  
  
button {  
  padding: 12px 28px;  
  border-radius: 30px;  
  border: none;  
  background: #e63946;  
  color: white;  
  font-size: 16px;  
  cursor: pointer;  
}  
  
img {  
  width: 85%;  
  max-width: 320px;  
  border-radius: 18px;  
  margin: 20px 0;  
}  
  
/* Music button */  
#musicBtn {  
  position: fixed;  
  bottom: 20px;  
  right: 20px;  
  background: #e63946;  
  color: white;  
  border: none;  
  width: 55px;  
  height: 55px;  
  border-radius: 50%;  
  font-size: 22px;  
  cursor: pointer;  
  box-shadow: 0 4px 10px rgba(0,0,0,0.3);  
}  
</style>  
</head>  
  
<body>  
  
<!-- Background Music -->  
<audio id="music" loop>  
  <source src="Blue.mp3.mp3" type="audio/mpeg">  
</audio>  
<button id="musicBtn">🔇</button>  
  
<!-- Screens -->  
  
<div class="screen active">  
  <h2>This is a message for the person</h2>  
  <p>who means more to me than she’ll ever realize 💕</p>  
  <button onclick="next()">Next →</button>  
</div>  
  
<div class="screen">  
  <h1>Hi Manyaaa 🎂💖</h1>  
  <button onclick="next()">Next →</button>  
</div>  
  
<div class="screen">  
  <p>Some people come into our lives quietly</p>  
  <p>and end up changing everything 🌷</p>  
  <button onclick="next()">Next →</button>  
</div>  
  
<div class="screen">  
  <h2>Our Memories 🥹💞</h2>  
  <img src="photo1.jpg.jpg">  
  <img src="photo2.jpg.jpg">  
  <img src="photo3.jpg.jpg">  
  <img src="photo4.jpg.jpg">  
  <img src="photo5.jpg.jpg">  
  <button onclick="next()">Next →</button>  
</div>  
  
<div class="screen">  
  <p>I don’t say this enough,</p>  
  <p>but I’m really lucky to have you 🤍</p>  
  <button onclick="next()">Next →</button>  
</div>  
  
<div class="screen">  
  <h2>To Manyaaa,</h2>  
  <p>  
    Happy Birthday — Feb 13 🎉<br><br>  
    You mean more to me than words can explain.<br>  
    Thank you for being you.<br><br>  
    Always here 🤍  
  </p>  
  <button onclick="next()">Next →</button>  
</div>  
  
<div class="screen">  
  <h2>Best friends forever ♾️💗</h2>  
  <p>Always. No matter what.</p>  
</div>  
  
<script>  
let i = 0;  
const screens = document.querySelectorAll('.screen');  
const music = document.getElementById('music');  
const btn = document.getElementById('musicBtn');  
  
function next() {  
  screens[i].classList.remove('active');  
  i++;  
  if (i < screens.length) {  
    screens[i].classList.add('active');  
  }  
}  
  
btn.onclick = () => {  
  if (music.paused) {  
    music.play();  
    btn.textContent = "🔊";  
  } else {  
    music.pause();  
    btn.textContent = "🔇";  
  }  
};  
</script>  
  
</body>  
</html>  
