<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vault Squad | Fortnite Clan</title>
  <style>
    :root{
      --bg:#06131d;
      --panel:#0d1d2b;
      --panel2:#102b3d;
      --green:#74f1b3;
      --yellow:#ffd166;
      --orange:#ff9c43;
      --red:#ff5d7a;
      --text:#edf7ff;
      --muted:#b8d1e7;
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0; font-family:Segoe UI, Arial, sans-serif; background:
        radial-gradient(circle at top, rgba(69,117,255,.22), transparent 22%),
        linear-gradient(180deg,#07131d,#040b10 60%);
      color:var(--text);
    }
    body::before{
      content:""; position:fixed; inset:0; pointer-events:none;
      background-image:radial-gradient(2px 2px at 10% 20%, rgba(255,255,255,.6), transparent 100%), radial-gradient(2px 2px at 50% 60%, rgba(255,255,255,.4), transparent 100%), radial-gradient(2px 2px at 80% 22%, rgba(255,255,255,.7), transparent 100%);
      opacity:.8;
    }
    .wrap{max-width:1180px; margin:0 auto; padding:20px 20px 70px; position:relative; z-index:1}
    nav{
      display:flex; justify-content:space-between; align-items:center; gap:18px;
      padding:18px 0 26px;
    }
    .logo{font-size:1.5rem; font-weight:900; letter-spacing:.2em; text-transform:uppercase}
    .logo span{color:var(--yellow)}
    .navlinks{display:flex; gap:20px; flex-wrap:wrap; color:var(--muted); font-size:.82rem; letter-spacing:.12em; text-transform:uppercase}
    .navlinks a{color:inherit; text-decoration:none}
    .cta{padding:12px 18px; border-radius:999px; border:none; font-weight:900; background:linear-gradient(135deg,var(--yellow),var(--orange)); color:#101821; cursor:pointer}
    .hero{display:grid; grid-template-columns:1.2fr .8fr; gap:30px; align-items:center; padding:30px 0 20px}
    .eyebrow{
      display:inline-block; padding:8px 14px; border-radius:999px; font-size:.72rem; font-weight:900; letter-spacing:.18em; text-transform:uppercase;
      background:rgba(116,241,179,.1); border:1px solid rgba(116,241,179,.5); color:var(--green)
    }
    h1{font-size:clamp(2.9rem,6vw,5.5rem); line-height:1; margin:18px 0 16px; letter-spacing:-.04em}
    h1 span{color:var(--yellow)}
    .hero p{max-width:620px; color:var(--muted); font-size:1.1rem; line-height:1.8}
    .hero-actions{display:flex; gap:14px; flex-wrap:wrap; margin-top:24px}
    .primary,.secondary{padding:16px 22px; border-radius:999px; font-weight:900; border:none; cursor:pointer}
    .primary{background:linear-gradient(135deg,var(--yellow),var(--orange)); color:#111b22}
    .secondary{background:rgba(255,255,255,.04); border:1px solid rgba(255,255,255,.1); color:var(--text)}
    .stats{display:grid; grid-template-columns:repeat(3,1fr); gap:14px; margin-top:28px}
    .stat{background:rgba(255,255,255,.04); border:1px solid rgba(255,255,255,.08); border-radius:16px; padding:18px 16px; text-align:center}
    .stat strong{display:block; font-size:2rem; color:var(--yellow); margin-bottom:4px}
    .stat span{color:var(--muted); font-size:.8rem; letter-spacing:.12em; text-transform:uppercase}
    .card{
      padding:24px; border-radius:24px; background:linear-gradient(180deg,rgba(16,43,61,.9), rgba(8,20,29,.8));
      border:1px solid rgba(255,255,255,.08); box-shadow:0 20px 45px rgba(0,0,0,.35)
    }
    .mini-box{padding:16px; border-radius:18px; background:rgba(255,255,255,.04); border:1px solid rgba(255,255,255,.08); margin-bottom:16px}
    .mini-box h3{margin:0 0 10px; font-size:.75rem; letter-spacing:.18em; text-transform:uppercase; color:var(--green)}
    .mini-box .big{font-size:2.2rem; font-weight:900; color:var(--text)}
    .mini-box .small{font-size:.9rem; color:var(--muted)}
    .game-box{margin-top:26px; padding:22px; border-radius:28px; background:linear-gradient(180deg,rgba(8,17,24,.9), rgba(18,35,48,.9)); border:1px solid rgba(255,255,255,.08)}
    .game-top{display:flex; justify-content:space-between; align-items:center; margin-bottom:16px}
    .game-top h2{margin:0; font-size:1.6rem}
    .score-pill{padding:8px 12px; border-radius:999px; background:rgba(116,241,179,.12); border:1px solid rgba(116,241,179,.5); color:var(--green); font-size:.8rem; font-weight:800}
    #spaceGame{position:relative; height:180px; margin-top:10px; border-radius:18px; border:1px solid rgba(255,255,255,.08); background:linear-gradient(180deg,#091720,#0f1f2d); overflow:hidden}
    .track{position:absolute; left:20px; right:20px; top:50%; transform:translateY(-50%); height:12px; border-radius:999px; background:rgba(255,255,255,.06); border:1px solid rgba(255,255,255,.08)}
    .center-line{position:absolute; top:18px; bottom:18px; left:50%; width:12px; transform:translateX(-50%); background:rgba(255,255,255,.7); border-radius:999px; box-shadow:0 0 14px rgba(255,255,255,.6)}
    .runner{position:absolute; top:50%; left:0; width:18px; height:86px; transform:translateY(-50%); background:linear-gradient(180deg,#74f1b3,#3dd6c1); border-radius:999px; box-shadow:0 0 18px rgba(116,241,179,.6)}
    .message{margin-top:12px; color:var(--muted); min-height:24px}
    .button-row{display:flex; gap:12px; flex-wrap:wrap; margin-top:18px}
    .play-btn{padding:14px 20px; border:none; border-radius:999px; background:linear-gradient(135deg,var(--yellow),var(--orange)); font-weight:900; cursor:pointer; color:#101821}
    .section{margin-top:50px; display:grid; grid-template-columns:1fr 1fr; gap:24px}
    .feature, .join-box{background:rgba(255,255,255,.04); border:1px solid rgba(255,255,255,.08); border-radius:22px; padding:24px}
    .feature h3, .join-box h3{margin-top:0; font-size:1.5rem}
    ul{margin:0; padding-left:18px; color:var(--muted); line-height:2}
    form{display:grid; gap:12px; margin-top:18px}
    input, select{padding:14px 15px; border-radius:12px; border:1px solid rgba(255,255,255,.12); background:rgba(255,255,255,.02); color:var(--text)}
    .join-btn{margin-top:6px; padding:15px 18px; border:none; border-radius:12px; background:linear-gradient(135deg,var(--green),#48d7b4); color:#06211a; font-weight:900; cursor:pointer}
    footer{margin-top:54px; text-align:center; color:var(--muted); font-size:.8rem; letter-spacing:.12em; text-transform:uppercase}
    @media (max-width:850px){
      .hero, .section{grid-template-columns:1fr}
      .stats{grid-template-columns:1fr}
      nav{flex-direction:column; align-items:flex-start}
      .logo{letter-spacing:.12em}
    }
  </style>
</head>
<body>
  <div class="wrap">
    <nav>
      <div class="logo">Vault <span>Squad</span></div>
      <div class="navlinks">
        <a href="#about">About</a>
        <a href="#game">Game</a>
        <a href="#join">Join</a>
      </div>
      <button class="cta">Apply Now</button>
    </nav>

    <header class="hero" id="about">
      <div>
        <div class="eyebrow">Fortnite Clan</div>
        <h1>Join a squad built for <span>wins</span>.</h1>
        <p>Vault Squad is a competitive Fortnite clan for players who want to win scrims, build strong teamwork, and grind the battle pass together. We focus on communication, strategy, and having fun every match.</p>
        <div class="hero-actions">
          <button class="primary" onclick="document.getElementById('join').scrollIntoView({behavior:'smooth'}); alert('A tester will try you at the next clan scrim.');">Join the Clan</button>
          <button class="secondary" onclick="alert('You must have at least 35 wins, be active, and have a strong average K/D ratio to join this Fortnite clan.');">View Requirements</button>
        </div>
        <div class="stats">
          <div class="stat"><strong>1.8K</strong><span>Members</span></div>
          <div class="stat"><strong>92%</strong><span>Win Rate</span></div>
          <div class="stat"><strong>24/7</strong><span>Voice Chat</span></div>
        </div>
      </div>

      <div class="card">
        <div class="mini-box">
          <h3>Clan Rank</h3>
          <div class="big">Diamond</div>
          <div class="small">Top 1% seasonal push</div>
        </div>
        <div class="mini-box">
          <h3>Current Goal</h3>
          <div class="big">Victory</div>
          <div class="small">Fortnite tournaments + scrim nights</div>
        </div>
        <div class="mini-box">
          <h3>Recruitment</h3>
          <div class="big">Open</div>
          <div class="small">Looking for active players</div>
        </div>
      </div>
    </header>

    <section class="game-box" id="game">
      <div class="game-top">
        <h2>Spacebar Timing Challenge</h2>
        <div class="score-pill" id="statusText">Ready</div>
      </div>
      <div id="spaceGame">
        <div class="track"></div>
        <div class="center-line"></div>
        <div class="runner" id="runner"></div>
      </div>
      <div class="message" id="message">Press the spacebar when the thin line hits the center line.</div>
      <div class="button-row">
        <button class="play-btn" id="startBtn">Start Challenge</button>
      </div>
    </section>

    <section class="section">
      <div class="feature">
        <h3>Why Join Vault Squad?</h3>
        <ul>
          <li>Daily scrims and ranked matches</li>
          <li>Friendly, skilled squad members</li>
          <li>Voice chat and team strategy</li>
          <li>Battle pass progression together</li>
          <li>Clan events and tournaments</li>
        </ul>
      </div>

      <div class="join-box" id="join">
        <h3>Apply to the Clan</h3>
        <form>
          <input type="text" placeholder="Epic Username" />
          <input type="text" placeholder="Discord Tag" />
          <select>
            <option>Platform</option>
            <option>PC</option>
            <option>PlayStation</option>
            <option>Xbox</option>
            <option>Mobile</option>
          </select>
          <input type="text" placeholder="Preferred Role" />
          <button class="join-btn" type="button" onclick="alert('A tester will try you at the next clan scrim.');">Send Application</button>
        </form>
      </div>
    </section>

    <footer>Vault Squad • building champions</footer>
  </div>

  <script>
    const runner = document.getElementById('runner');
    const statusText = document.getElementById('statusText');
    const startBtn = document.getElementById('startBtn');
    const message = document.getElementById('message');
    const gameBox = document.getElementById('spaceGame');

    let active = false;
    let score = 0;
    let runnerX = 0;
    let direction = 1;
    let speed = 8;
    let moveTimer = null;

    function updateRunner() {
      const maxX = gameBox.clientWidth - 20;
      runnerX += direction * speed;
      if (runnerX <= 0 || runnerX >= maxX) direction *= -1;
      runner.style.left = runnerX + 'px';
    }

    function startGame() {
      active = true;
      score = 0;
      runnerX = 0;
      direction = 1;
      speed = 8;
      statusText.textContent = 'Playing';
      message.textContent = 'Press the spacebar when the thin line hits the middle.';
      runner.style.left = '0px';
      clearInterval(moveTimer);
      moveTimer = setInterval(updateRunner, 24);
    }

    function stopGame() {
      active = false;
      clearInterval(moveTimer);
      statusText.textContent = 'Final: ' + score;
      message.textContent = 'Round complete! Final score: ' + score;
    }

    document.addEventListener('keydown', function(e) {
      if (e.code === 'Space') {
        e.preventDefault();
        if (!active) {
          startGame();
          return;
        }

        const centerX = gameBox.clientWidth / 2;
        const runnerCenter = runnerX + 2;
        const diff = Math.abs(runnerCenter - centerX);

        if (diff < 22) {
          score += 10;
          speed = Math.min(speed + 2.5, 22);
          statusText.textContent = 'Score: ' + score;
          message.textContent = 'Perfect timing!';
          runnerX = 0;
          direction = 1;
        } else {
          score = Math.max(0, score - 3);
          statusText.textContent = 'Score: ' + score;
          message.textContent = 'Too early or too late!';
        }
      }
    });

    startBtn.addEventListener('click', () => {
      if (active) {
        stopGame();
      } else {
        startGame();
      }
    });
  </script>
</body>
</html>

