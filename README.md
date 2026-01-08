# pinky-<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Shashank (Pinky), Please Read 💔💗</title>
<script src="https://cdn.jsdelivr.net/npm/html2canvas@1.4.1/dist/html2canvas.min.js"></script>
<style>
*{box-sizing:border-box;font-family:'Poppins',sans-serif}
body{margin:0;height:100vh;display:flex;align-items:center;justify-content:center;background:linear-gradient(135deg,#0e0007,#ff8fb1);overflow:hidden}
.card{background:rgba(255,192,203,.18);backdrop-filter:blur(14px);border-radius:28px;padding:42px 32px 36px;width:92%;max-width:520px;text-align:center;box-shadow:0 30px 70px rgba(0,0,0,.5);animation:float 4s ease-in-out infinite;position:relative}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-12px)}}
h1{color:#ffb6c1;margin:0 0 6px;font-size:2.2rem}
h2{color:#ffd1dc;font-size:1.15rem;margin:0 0 14px;font-weight:400}
p{color:#ffe6ee;font-size:1.05rem;line-height:1.65}
.emoji{font-size:3rem;margin:12px 0;animation:shake 1.2s infinite}
@keyframes shake{0%{transform:rotate(0)}25%{transform:rotate(-8deg)}50%{transform:rotate(8deg)}75%{transform:rotate(-8deg)}100%{transform:rotate(0)}}
button{margin-top:18px;background:#ff5c8d;border:none;color:#fff;padding:14px 30px;border-radius:999px;font-size:1rem;cursor:pointer;transition:.25s;box-shadow:0 12px 24px rgba(255,92,141,.45)}
button:hover{transform:scale(1.08);background:#ff2f73}
textarea{width:100%;min-height:110px;margin-top:16px;padding:12px 14px;border-radius:16px;border:1px solid rgba(255,182,193,.5);background:rgba(0,0,0,.2);color:#ffe6ee;resize:none;outline:none}
.hidden{display:none}
.letter{margin-top:16px;padding:16px;border-radius:18px;background:rgba(0,0,0,.3);border:1px solid rgba(255,182,193,.35);text-align:left;font-style:italic;max-height:150px;overflow-y:auto}
.hearts span{position:absolute;color:pink;font-size:22px;animation:fall 6s linear infinite}
@keyframes fall{0%{transform:translateY(-10vh)}100%{transform:translateY(110vh);opacity:0}}
.stamp{position:absolute;top:14px;right:14px;transform:rotate(-12deg);padding:6px 10px;border-radius:8px;border:2px solid #ff8fb1;color:#ff8fb1;font-weight:700;background:rgba(0,0,0,.25)}
.music{position:absolute;bottom:14px;left:14px;font-size:.85rem;color:#ffd1dc;opacity:.8}
</style>
</head>
<body>
<audio id="bgm" src="dhooram.mp3" autoplay loop></audio>
<div class="card" id="capture">
<div class="stamp">READ ME</div>
<h1>Shashank.</h1>
<h2>(Pinky)</h2>
<div class="emoji">💔😠💗</div>
<p>I need you to read this properly.</p>
<button onclick="reveal()">I will read 🥺</button>

<div id="letter" class="letter hidden" onscroll="unlockReply()">
“nenu niku monna call chesi napudu and like from few days i feel you dont love me idk that thought literally is haunting me every sec i really love you ik you have your exams and you are busy but i also do know you are not preparing like for 24/7 whole day long you can spend like atleast 5mins and i feel so bad and sad for asking you for bare minimum, why do you never understand what i feel or do you just ignore even when you understand....gadida i really love you i'm sorry for being annoying but idk i miss you a lot like a lot!!”
</div>

<textarea id="reply" class="hidden" placeholder="Write a message back to me (minimum 25 words)…"></textarea>
<button id="sendReply" class="hidden" onclick="sendReply()">Send to Me 💔</button>
<div class="music">🎵 Dhooram – Arjun Reddy (soft)</div>
</div>
<script>
// unlock music gently
const bgm=document.getElementById('bgm'); bgm.volume=0.25;
function reveal(){document.getElementById('letter').classList.remove('hidden')}
function unlockReply(){const el=document.getElementById('letter');if(el.scrollTop+el.clientHeight>=el.scrollHeight-5){document.getElementById('reply').classList.remove('hidden');document.getElementById('sendReply').classList.remove('hidden')}}
function sendReply(){const text=document.getElementById('reply').value.trim();const words=text.split(/\s+/).length;if(words<25){alert('Please write at least 25 words. Mean it.');return;}
// auto-save
localStorage.setItem('pinky_reply', text);
// screenshot
html2canvas(document.getElementById('capture')).then(canvas=>{
const link=document.createElement('a');link.download='pinky_reply.png';link.href=canvas.toDataURL();link.click();});
alert('Now my turn to apologize 💗\nYou send me lot of kisses 😘😘😘');createHearts(40)}
function createHearts(n){for(let i=0;i<n;i++){const h=document.createElement('span');h.innerHTML='💗';h.style.left=Math.random()*100+'vw';h.style.animationDuration=(Math.random()*3+3)+'s';document.body.appendChild(h);setTimeout(()=>h.remove(),6000)}}
</script>
</body>
</html>
