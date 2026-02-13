<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Hacked System Terminal</title>
<style>
body {
  margin: 0;
  overflow: auto;
  font-family: 'Courier New', monospace;
  color: #00ff00;
  background: #000;
}

/* Matrix Background */
.matrix-bg {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}

/* CENTER CONTAINER - Enhanced for hack look with more animations */
.container {
  width: 700px;
  margin: 50px auto;
  text-align: center;
  background: rgba(0, 0, 0, 0.9);
  padding: 30px;
  border-radius: 10px;
  border: 2px solid #ff0000;
  box-shadow: 0 0 30px rgba(255, 0, 0, 0.8), inset 0 0 20px rgba(255, 0, 0, 0.3);
  position: relative;
  animation: containerGlow 2s infinite alternate, fadeIn 2s ease-in;
  transition: transform 0.3s ease;
  z-index: 1;
}

.container:hover {
  transform: scale(1.02);
}

@keyframes containerGlow {
  0% { box-shadow: 0 0 30px rgba(255, 0, 0, 0.8), inset 0 0 20px rgba(255, 0, 0, 0.3); }
  100% { box-shadow: 0 0 50px rgba(255, 0, 0, 1), inset 0 0 30px rgba(255, 0, 0, 0.5); }
}

@keyframes fadeIn {
  0% { opacity: 0; transform: translateY(20px); }
  100% { opacity: 1; transform: translateY(0); }
}

.container::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 5px;
  background: linear-gradient(90deg, #ff0000, #00ff00, #0000ff);
  animation: scan 2s linear infinite;
}

@keyframes scan {
  0% { transform: translateX(-100%); }
  100% { transform: translateX(100%); }
}

/* IMAGE - Avatar with enhanced glitch effect - Made bigger */
.avatar {
  width: 200px;
  height: 266px;
  border-radius: 100px;
  border: 3px solid #ff0000;
  box-shadow: 0 0 20px #ff0000;
  object-fit: cover;
  position: relative;
  animation: glitch 1s infinite, avatarRotate 5s linear infinite;
  transition: box-shadow 0.5s ease;
}

.avatar:hover {
  box-shadow: 0 0 30px #ff0000;
}

@keyframes glitch {
  0%, 100% { transform: translate(0); }
  20% { transform: translate(-2px, 2px); }
  40% { transform: translate(-2px, -2px); }
  60% { transform: translate(2px, 2px); }
  80% { transform: translate(2px, -2px); }
}

@keyframes avatarRotate {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

/* TITLE - Larger and more prominent with enhanced flickering and shake */
h1 {
  color: #00ffff;
  text-shadow: 0 0 10px #ff0000, 0 0 20px #ff0000;
  margin-top: 20px;
  font-size: 60px; /* Increased from 48px */
  animation: flicker 1.5s infinite alternate, shake 0.5s infinite;
  transition: color 0.3s ease;
}

h1:hover {
  color: #ffff00;
}

@keyframes flicker {
  0% { opacity: 1; }
  50% { opacity: 0.5; }
  100% { opacity: 1; }
}

@keyframes shake {
  0%, 100% { transform: translateX(0); }
  10% { transform: translateX(-2px); }
  20% { transform: translateX(2px); }
  30% { transform: translateX(-2px); }
  40% { transform: translateX(2px); }
  50% { transform: translateX(-2px); }
  60% { transform: translateX(2px); }
  70% { transform: translateX(-2px); }
  80% { transform: translateX(2px); }
  90% { transform: translateX(-2px); }
}

/* TAG - Larger terminal style with pulse */
.tag {
  border: 2px solid #00ff00;
  display: inline-block;
  padding: 10px 25px;
  margin: 15px 0;
  background: rgba(0, 0, 0, 0.8);
  font-weight: bold;
  color: #00ff00;
  text-transform: uppercase;
  letter-spacing: 2px;
  box-shadow: 0 0 10px #00ff00;
  font-size: 20px; /* Increased from 18px */
  animation: tagPulse 2s infinite alternate;
  transition: background 0.3s ease;
}

.tag:hover {
  background: rgba(0, 255, 0, 0.2);
}

@keyframes tagPulse {
  0% { box-shadow: 0 0 10px #00ff00; }
  100% { box-shadow: 0 0 20px #00ff00; }
}

/* TERMINAL LINES - Slightly larger with typing effect */
.terminal-lines {
  font-size: 16px; /* Increased from 14px */
  color: #00ff00;
  margin-bottom: 10px;
  overflow: hidden;
  white-space: nowrap;
  animation: typing 3s steps(40, end) forwards;
}

.terminal-lines::before {
  content: '$ ';
  color: #ffff00;
}

@keyframes typing {
  from { width: 0; }
  to { width: 100%; }
}

/* PROGRESS BAR - Enhanced with more dynamic animation */
.progress {
  width: 100%;
  height: 10px;
  background: rgba(255, 255, 255, 0.1);
  border: 1px solid #00ff00;
  margin: 20px 0;
  overflow: hidden;
  animation: progressGlow 1s infinite alternate;
}

.progress-bar {
  height: 100%;
  background: linear-gradient(90deg, #00ff00, #ffff00, #ff0000);
  width: 0%;
  animation: progress 5s ease-in-out infinite, progressShimmer 1s infinite;
}

@keyframes progress {
  0% { width: 0%; }
  50% { width: 70%; }
  100% { width: 100%; }
}

@keyframes progressGlow {
  0% { border-color: #00ff00; }
  100% { border-color: #ffff00; }
}

@keyframes progressShimmer {
  0% { background-position: -100% 0; }
  100% { background-position: 100% 0; }
}

/* MESSAGE BOX - Larger text with enhanced effects */
.box {
  border: 2px solid #ff0000;
  margin-top: 20px;
  padding: 20px;
  background: rgba(0, 0, 0, 0.8);
  font-size: 22px; /* Increased from 20px */
  line-height: 1.6;
  box-shadow: 0 0 15px rgba(255, 0, 0, 0.5) inset;
  position: relative;
  display: inline-block;
  text-align: left;
  animation: boxBounce 2s infinite alternate;
  transition: border-color 0.3s ease;
}

.box:hover {
  border-color: #ffff00;
}

@keyframes boxBounce {
  0% { transform: translateY(0); }
  100% { transform: translateY(-5px); }
}

.box::after {
  content: '>';
  position: absolute;
  bottom: 10px;
  right: 10px;
  color: #00ff00;
  font-size: 24px;
  animation: blink 1s infinite, cursorGlow 1s infinite alternate;
}

@keyframes blink {
  0%, 50% { opacity: 1; }
  51%, 100% { opacity: 0; }
}

@keyframes cursorGlow {
  0% { text-shadow: 0 0 5px #00ff00; }
  100% { text-shadow: 0 0 15px #00ff00; }
}

/* Customized "DEAR ADMIN" - Made cooler with red glow, uppercase, and pulse animation */
.dear-admin {
  color: #ff0000;
  font-size: 26px; /* Increased from 24px */
  font-weight: bold;
  text-transform: uppercase;
  text-shadow: 0 0 10px #ff0000, 0 0 20px #ff0000;
  animation: adminPulse 1.5s infinite alternate, adminGlow 2s infinite;
  display: inline-block;
  margin-bottom: 10px;
}

@keyframes adminPulse {
  0% { transform: scale(1); }
  100% { transform: scale(1.05); }
}

@keyframes adminGlow {
  0% { text-shadow: 0 0 10px #ff0000, 0 0 20px #ff0000; }
  50% { text-shadow: 0 0 15px #ff0000, 0 0 30px #ff0000; }
  100% { text-shadow: 0 0 10px #ff0000, 0 0 20px #ff0000; }
}

/* Enhanced message text - Added subtle color variation and animation */
.message-text {
  color: #ffff00;
  text-shadow: 0 0 5px #ffff00;
  animation: textFlicker 3s infinite alternate;
}

@keyframes textFlicker {
  0% { opacity: 1; }
  50% { opacity: 0.8; }
  100% { opacity: 1; }
}

/* FOOTER - Slightly larger with fade effect */
.footer {
  margin-top: 20px;
  color: #ff4d4d;
  font-size: 16px; /* Increased from 14px */
  text-shadow: 0 0 5px #ff4d4d;
  animation: footerFade 3s infinite alternate;
}

@keyframes footerFade {
  0% { opacity: 0.7; }
  100% { opacity: 1; }
}
</style>
</head>
<body>
<!-- Matrix Background Canvas -->
<canvas id="matrix-bg" class="matrix-bg"></canvas>

<!-- Audio element with external link -->
<audio id="bgMusic" loop preload="auto">
    <source src="https://files.catbox.moe/4mfap1.mp3" type="audio/mpeg">
</audio>

<div class="container">
  <img src="https://l.top4top.io/p_3692bsfeq1.jpg" class="avatar">
  <h1>SECURITY BREACH DETECTED H4CK3D BY RL😈</h1>
  <div class="tag">UNAUTHORIZED ACCESS GRANTED | INDIAN BLACK HAT😈</div>
  <div class="terminal-lines">root@compromised:~# Initializing breach protocol...</div>
  <div class="terminal-lines">root@compromised:~# Accessing root directory...</div>
  <div class="terminal-lines">root@compromised:~# Decrypting files...</div>
  <div class="progress">
    <div class="progress-bar"></div>
  </div>
  <div class="box">
    <span class="dear-admin">ATTENTION SYSTEM ADMINISTRATOR</span>,<br><br>
    <span class="message-text">Sorry Admin, Your Website has been infiltrated. Testing Purposes Only</span><br><br>
    - RL
  </div>
  <div class="footer">© Security Researcher | Penetration Testing</div>
</div>

<script>
// Matrix Rain Effect with Alternative Lightning: Pulsing Electric Grid
const canvas = document.getElementById('matrix-bg');
const ctx = canvas.getContext('2d');

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const matrixChars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789@#$%^&*()_+-=[]{}|;:,.<>?';
const fontSize = 14;
const columns = canvas.width / fontSize;
const drops = [];

for (let x = 0; x < columns; x++) {
  drops[x] = 1;
}

let gridTimer = 0;
let gridActive = false;

function drawElectricGrid() {
  ctx.strokeStyle = '#ffffff';
  ctx.lineWidth = 1;
  ctx.shadowColor = '#ffffff';
  ctx.shadowBlur = 10;
  ctx.globalAlpha = 0.5;

  // Horizontal lines
  for (let y = 0; y < canvas.height; y += 50) {
    ctx.beginPath();
    ctx.moveTo(0, y);
    ctx.lineTo(canvas.width, y);
    ctx.stroke();
  }

  // Vertical lines
  for (let x = 0; x < canvas.width; x += 50) {
    ctx.beginPath();
    ctx.moveTo(x, 0);
    ctx.lineTo(x, canvas.height);
    ctx.stroke();
  }

  ctx.globalAlpha = 1;
  ctx.shadowBlur = 0;
}

function draw() {
  ctx.fillStyle = 'rgba(0, 0, 0, 0.04)';
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  gridTimer++;
  if (gridTimer > 120) { // Trigger grid every ~4 seconds
    gridActive = true;
    gridTimer = 0;
  }

  if (gridActive) {
    drawElectricGrid();
    if (gridTimer > 10) { // Show for a short time
      gridActive = false;
    }
  }

  ctx.fillStyle = '#00ff00';
  ctx.font = fontSize + 'px monospace';

  for (let i = 0; i < drops.length; i++) {
    const text = matrixChars.charAt(Math.floor(Math.random() * matrixChars.length));
    ctx.fillText(text, i * fontSize, drops[i] * fontSize);

    if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
      drops[i] = 0;
    }
    drops[i]++;
  }
}

setInterval(draw, 35);

// Aggressive autoplay JS
(function() {
    const audio = document.getElementById('bgMusic');
    let attempts = 0;
    const maxAttempts = 50;
    
    function forcePlay() {
        audio.play().then(() => {
            console.log('Autoplay forced successfully!');
        }).catch((error) => {
            console.log('Autoplay blocked, retrying...', error);
            if (attempts < maxAttempts) {
                attempts++;
                setTimeout(forcePlay, 100);
            } else {
                console.log('Max attempts reached. Autoplay blocked by browser.');
            }
        });
    }
    // Start trying on DOMContentLoaded
    document.addEventListener('DOMContentLoaded', forcePlay);
})();
</script>
</body>
</html>
