<!doctype html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Vault Squad</title>
<style>
body{margin:0;font-family:Arial,sans-serif;background:radial-gradient(circle at top,#0d1d2a,#07131b 45%,#030b10);color:#effbff}*{box-sizing:border-box}.wrap{max-width:900px;margin:40px auto;padding:32px;border-radius:24px;background:rgba(19,45,61,.82);box-shadow:0 18px 50px rgba(0,0,0,.3);border:1px solid rgba(255,255,255,.12)}.tag{display:inline-block;padding:8px 14px;border-radius:999px;background:rgba(100,245,183,.12);border:1px solid rgba(100,245,183,.5);color:#64f5b7;font-weight:700;letter-spacing:.12em;text-transform:uppercase;font-size:.7rem}h1{margin:14px 0 10px;font-size:clamp(2.8rem,7vw,4.5rem)}p{margin:0;line-height:1.7;color:#dfeef5}.row{display:flex;gap:12px;flex-wrap:wrap;margin:20px 0}.btn{padding:12px 20px;border:none;border-radius:999px;background:linear-gradient(135deg,#f7d15d,#ffb866);color:#07131b;font-weight:800;cursor:pointer}.btn.alt{background:rgba(255,255,255,.08);color:#effbff;border:1px solid rgba(255,255,255,.12)}.info{margin:14px 0;display:flex;gap:16px;flex-wrap:wrap;font-weight:700}.info b{color:#f7d15d}canvas{display:block;width:100%;height:auto;border-radius:16px;background:#07131b;border:1px solid rgba(255,255,255,.08)}
</style>
</head>
<body>
<div class="wrap">
<span class="tag">Clan Tag: VLT</span>
<h1>Vault Squad</h1>
<p>Competitive Fortnite-style clan built for fast movers, smart team play, and clutch wins.</p>
<div class="row"><button class="btn">Play Now</button><button class="btn alt">Join Squad</button></div>
<div class="info">Score <b id="s">0</b> | Time <b id="t">20</b>s</div>
<canvas id="c" width="760" height="420"></canvas>
</div>
<script>
const c=document.getElementById('c'),ctx=c.getContext('2d'),s=document.getElementById('s'),t=document.getElementById('t');
let score=0,time=20,target=null;
function spawn(){target={x:50+Math.random()*(c.width-100),y:50+Math.random()*(c.height-100),r:24+Math.random()*18}}
function draw(){ctx.clearRect(0,0,c.width,c.height);ctx.fillStyle='#0a1b24';ctx.fillRect(0,0,c.width,c.height);if(target){ctx.beginPath();ctx.fillStyle='#64f5b7';ctx.arc(target.x,target.y,target.r,0,Math.PI*2);ctx.fill();ctx.beginPath();ctx.fillStyle='#effbff';ctx.arc(target.x,target.y,target.r*.38,0,Math.PI*2);ctx.fill();}requestAnimationFrame(draw)}
c.onclick=e=>{const r=c.getBoundingClientRect();const x=((e.clientX-r.left)/r.width)*c.width;const y=((e.clientY-r.top)/r.height)*c.height;if(!target)return;const d=Math.hypot(x-target.x,y-target.y);if(d<target.r){score++;s.textContent=score;spawn()}else score=Math.max(0,score-1),s.textContent=score};
setInterval(()=>{if(time>0){time-=.1;t.textContent=Math.max(0,time.toFixed(1))}else{alert('Final score: '+score);time=20;score=0;s.textContent=0;t.textContent='20'}},100);
spawn();draw();
</script>
</body>
</html>
