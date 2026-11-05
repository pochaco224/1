
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SWEET CONFESSION - 11.11</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Jua&family=Noto+Sans+KR:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">

<style>
:root {
  --pink:#ff8fc5;
  --hot:#f36cae;
  --pale:#ffe8f2;
  --purple:#b7a8bd;
  --ink:#554b5a;
  --white:#fffaff;
}

* {
  margin:0;
  padding:0;
  box-sizing:border-box;
}

html {
  scroll-behavior:smooth;
  scroll-padding-top:85px;
}

body {
  font-family:'Noto Sans KR',sans-serif;
  background:#c9bbc9;
  color:var(--ink);
  overflow-x:hidden;
}

button {
  font-family:inherit;
}

.bg {
  position:fixed;
  inset:0;
  z-index:-3;
  background:
    radial-gradient(ellipse at 20% 20%,#f9d8e9,transparent 40%),
    radial-gradient(ellipse at 90% 80%,#b7a8bd,transparent 45%),
    linear-gradient(135deg,#a99baa,#e9dce8,#b9a9bc);
}

.bg::after {
  content:"";
  position:absolute;
  inset:0;
  backdrop-filter:blur(35px);
  background:#ffffff22;
}

.noise {
  position:fixed;
  inset:0;
  z-index:15;
  pointer-events:none;
  opacity:.09;
  background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='3'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.5'/%3E%3C/svg%3E");
}

/* HEADER */

header {
  position:fixed;
  top:0;
  left:0;
  width:100%;
  height:70px;
  z-index:30;
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:0 6%;
  background:#ffffffa6;
  backdrop-filter:blur(18px);
  border-bottom:1px solid #ffffff9c;
}

.brand {
  font-family:'Jua',sans-serif;
  font-size:20px;
  color:#ec78b2;
  letter-spacing:1px;
}

nav {
  display:flex;
  gap:25px;
}

nav a {
  text-decoration:none;
  color:#867586;
  font-size:10px;
  font-weight:700;
  letter-spacing:1.5px;
  transition:.3s;
}

nav a:hover {
  color:#ef72ad;
}

/* HERO */

.hero {
  min-height:100vh;
  padding:110px 8% 65px;
  display:flex;
  align-items:center;
  justify-content:center;
}

.hero-inner {
  width:100%;
  max-width:1150px;
  min-height:680px;
  display:grid;
  grid-template-columns:1fr 1fr;
  align-items:center;
  position:relative;
  border:1px solid #ffffffa8;
  background:#ffffff23;
  backdrop-filter:blur(15px);
  box-shadow:0 25px 80px #47364b24;
  overflow:hidden;
}

.hero-copy {
  padding:45px;
  position:relative;
  z-index:3;
}

.eyebrow {
  font-size:10px;
  letter-spacing:5px;
  font-weight:800;
  color:#d879aa;
}

.hero h1 {
  font-family:'Jua',sans-serif;
  font-size:clamp(58px,8vw,105px);
  line-height:1.12;
  margin:30px 0 22px;
  color:#fff;
  -webkit-text-stroke:1px #ed83b8;
  text-shadow:
    0 0 8px #ffb4d6,
    0 0 22px #ff83bd,
    0 0 45px #f36cae;
  transform:rotate(-3deg);
}

.hero h1 span {
  display:block;
  color:#ffacd1;
  margin-left:45px;
}

.hero-description {
  font-size:12px;
  line-height:2.2;
  color:#786b7b;
  margin-top:35px;
}

.hero-description strong {
  color:#ed71aa;
}

.enter {
  margin-top:35px;
  padding:15px 30px;
  background:#ed7ab1;
  color:white;
  border:1px solid #fff;
  border-radius:3px;
  font-size:11px;
  letter-spacing:2px;
  cursor:pointer;
  box-shadow:0 6px 22px #ef77b355;
  transition:.3s;
}

.enter:hover {
  background:#e65c9f;
  transform:translateY(-4px);
}

.hero-art {
  position:relative;
  height:650px;
  display:flex;
  justify-content:center;
  align-items:center;
}

.hero-art::before {
  content:"";
  position:absolute;
  width:78%;
  height:90%;
  background:#fff;
  transform:rotate(3deg);
  box-shadow:0 15px 40px #53445533;
}

.hero-art img {
  position:relative;
  z-index:2;
  width:85%;
  height:94%;
  object-fit:contain;
  filter:drop-shadow(0 12px 12px #4e394d24);
}

.hero-art img[src="character.png"] {
  object-fit:contain;
}

.art-caption {
  position:absolute;
  z-index:4;
  bottom:25px;
  right:8%;
  background:#fff;
  color:#ed79af;
  padding:12px 20px;
  font-family:'Jua',sans-serif;
  font-size:19px;
  transform:rotate(-5deg);
  box-shadow:0 5px 20px #513b4b22;
}

.floating-text {
  position:absolute;
  color:#fff;
  text-shadow:0 0 12px #f16fae;
  font-family:'Jua',sans-serif;
  z-index:4;
}

.ft1 {
  top:8%;
  left:5%;
  font-size:25px;
  transform:rotate(-12deg);
}

.ft2 {
  top:40%;
  right:2%;
  font-size:22px;
  transform:rotate(12deg);
}

.hero-number {
  position:absolute;
  bottom:25px;
  left:35px;
  font-size:10px;
  color:#ad94a9;
  letter-spacing:4px;
}

/* COMMON */

section {
  padding:120px 8%;
  position:relative;
}

.section-head {
  text-align:center;
  margin-bottom:55px;
}

.section-en {
  color:#e875aa;
  font-size:10px;
  letter-spacing:5px;
  font-weight:800;
}

.section-head h2 {
  font-family:'Jua',sans-serif;
  font-size:43px;
  margin:15px 0;
  color:#5e5060;
}

.section-head p {
  font-size:12px;
  color:#99879a;
  line-height:2;
}

/* STORY */

.story {
  background:#ffffff6b;
  backdrop-filter:blur(18px);
}

.story-layout {
  max-width:950px;
  margin:auto;
  display:grid;
  grid-template-columns:.75fr 1.25fr;
  gap:35px;
  align-items:stretch;
}

.story-side {
  min-height:430px;
  background:
    linear-gradient(#6b536c44,#6b536c44),
    linear-gradient(135deg,#e6b9d0,#a99cb3);
  display:flex;
  flex-direction:column;
  justify-content:space-between;
  padding:30px;
  color:white;
  position:relative;
  overflow:hidden;
}

.story-side::after {
  content:"11";
  position:absolute;
  right:-10px;
  bottom:-60px;
  font-family:'Jua',sans-serif;
  font-size:220px;
  opacity:.2;
}

.story-side small {
  font-size:10px;
  letter-spacing:3px;
}

.story-side strong {
  font-family:'Jua',sans-serif;
  font-size:35px;
  line-height:1.4;
  position:relative;
  z-index:2;
}

.story-side span {
  font-size:10px;
  letter-spacing:2px;
}

.story-content {
  background:#fffafde8;
  padding:45px;
  border:1px solid white;
  box-shadow:0 15px 40px #59445b13;
}

.story-content .tag {
  display:inline-block;
  padding:8px 15px;
  background:#ffe7f1;
  color:#df73a8;
  font-size:10px;
  letter-spacing:2px;
}

.story-content h3 {
  font-family:'Jua',sans-serif;
  font-size:27px;
  line-height:1.5;
  margin:25px 0;
}

.story-content p {
  color:#89798a;
  font-size:12px;
  line-height:2.5;
  white-space:pre-line;
}

.story-content p b {
  color:#e46b9f;
}

.story-footer {
  border-top:1px dashed #e8cbdc;
  margin-top:30px;
  padding-top:20px;
  display:flex;
  justify-content:space-between;
  color:#c18da9;
  font-size:10px;
  letter-spacing:2px;
}

/* CHARACTER */

.character {
  background:#e8dce55b;
}

.character-container {
  max-width:950px;
  margin:auto;
  background:#fffafde8;
  padding:35px;
  border:1px solid white;
  box-shadow:0 15px 55px #4e3d5018;
}

.character-top {
  display:flex;
  justify-content:space-between;
  align-items:center;
  border-bottom:1px solid #f1d9e5;
  padding-bottom:20px;
  margin-bottom:25px;
}

.character-top strong {
  font-family:'Jua',sans-serif;
  font-size:23px;
  color:#df76a9;
}

.character-top span {
  font-size:9px;
  letter-spacing:3px;
  color:#b49bad;
}

.character-grid {
  display:grid;
  grid-template-columns:250px 1fr;
  gap:35px;
}

.character-photo {
  position:relative;
  height:360px;
  background:linear-gradient(145deg,#f4d8e6,#ddd0df);
  padding:10px;
  border:1px solid #fff;
}

.character-photo img {
  width:100%;
  height:100%;
  object-fit:cover;
  object-position:center 20%;
}

.photo-label {
  position:absolute;
  bottom:20px;
  left:20px;
  padding:8px 12px;
  color:white;
  background:#e77eaecc;
  font-size:9px;
  letter-spacing:2px;
}

.character-info {
  display:flex;
  flex-direction:column;
}

.character-name {
  font-family:'Jua',sans-serif;
  font-size:37px;
  color:#645468;
  margin:8px 0;
}

.character-sub {
  font-size:10px;
  letter-spacing:3px;
  color:#cb8aaa;
  margin-bottom:25px;
}

.info-row {
  display:grid;
  grid-template-columns:105px 1fr;
  padding:13px 0;
  border-bottom:1px dashed #ead4e1;
  font-size:12px;
  line-height:1.8;
}

.info-row span:first-child {
  font-weight:800;
  color:#df7ba9;
}

.info-row span:last-child {
  color:#817184;
}

/* FAVORITE */

.favorites {
  max-width:950px;
  margin:30px auto 0;
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:15px;
}

.favorite-card {
  padding:25px;
  background:#ffffffbd;
  border:1px solid white;
}

.favorite-card span {
  color:#e57aaa;
  font-size:10px;
  letter-spacing:3px;
}

.favorite-card h4 {
  font-family:'Jua',sans-serif;
  margin:12px 0 5px;
  font-size:20px;
}

.favorite-card p {
  color:#958497;
  font-size:11px;
  line-height:2;
}

/* CHOICE */

.choice {
  background:#ffffff78;
  backdrop-filter:blur(18px);
}

.choice-box {
  max-width:750px;
  margin:auto;
  text-align:center;
  background:#fffafde8;
  padding:55px 30px;
  border:1px solid white;
  box-shadow:0 15px 40px #53405213;
}

.choice-box .mini {
  font-size:10px;
  letter-spacing:4px;
  color:#e87caf;
}

.choice-box h3 {
  font-family:'Jua',sans-serif;
  font-size:30px;
  line-height:1.5;
  margin:20px 0;
}

.choice-box p {
  font-size:12px;
  color:#9a899a;
  line-height:2;
}

.choices {
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
  gap:12px;
  margin-top:30px;
}

.choice-btn {
  padding:14px 25px;
  background:white;
  color:#d873a6;
  border:1px solid #efbfd6;
  cursor:pointer;
  font-size:12px;
  transition:.3s;
}

.choice-btn:hover {
  background:#ee83b6;
  color:white;
  transform:translateY(-3px);
}

.answer {
  margin:30px auto 0;
  max-width:500px;
  padding:20px;
  background:#ffeaf3;
  color:#bd6d99;
  font-size:13px;
  line-height:2;
  display:none;
}

.answer.show {
  display:block;
  animation:appear .4s ease;
}

@keyframes appear {
  from {opacity:0;transform:translateY(10px);}
  to {opacity:1;transform:translateY(0);}
}

/* SECRET */

.secret {
  max-width:800px;
  margin:70px auto 0;
  text-align:center;
}

.secret button {
  background:none;
  border:none;
  color:#e477ab;
  font-size:12px;
  cursor:pointer;
  letter-spacing:2px;
  border-bottom:1px solid #e477ab;
  padding:10px;
}

.secret-message {
  display:none;
  max-width:500px;
  margin:20px auto 0;
  padding:30px;
  background:#fff;
  color:#98788d;
  font-family:'Jua',sans-serif;
  font-size:20px;
  line-height:1.8;
  transform:rotate(-1deg);
  box-shadow:0 10px 30px #58435620;
}

.secret-message.show {
  display:block;
  animation:appear .5s ease;
}

/* FOOTER */

footer {
  padding:70px 20px;
  text-align:center;
  background:#ffffffa3;
  color:#a28da0;
  font-size:10px;
  letter-spacing:3px;
  line-height:2.5;
}

footer strong {
  display:block;
  font-family:'Jua',sans-serif;
  color:#ed80b5;
  font-size:28px;
  letter-spacing:1px;
}

/* SCROLL ANIMATION */

.reveal {
  opacity:0;
  transform:translateY(35px);
  transition:opacity .8s ease,transform .8s ease;
}

.reveal.visible {
  opacity:1;
  transform:translateY(0);
}

/* MOBILE */

@media(max-width:750px) {
  header {
    height:60px;
    padding:0 5%;
  }

  .brand {
    font-size:16px;
  }

  nav {
    gap:12px;
  }

  nav a {
    font-size:8px;
    letter-spacing:0;
  }

  .hero {
    padding:90px 5% 45px;
  }

  .hero-inner {
    grid-template-columns:1fr;
    min-height:auto;
  }

  .hero-copy {
    padding:35px 20px 15px;
    text-align:center;
  }

  .hero h1 {
    font-size:65px;
  }

  .hero h1 span {
    margin-left:0;
  }

  .hero-description {
    font-size:11px;
  }

  .hero-art {
    height:470px;
  }

  .hero-art img {
    width:85%;
  }

  .hero-number {
    display:none;
  }

  section {
    padding:90px 5%;
  }

  .section-head h2 {
    font-size:35px;
  }

  .story-layout {
    grid-template-columns:1fr;
  }

  .story-side {
    min-height:220px;
  }

  .story-content {
    padding:30px 23px;
  }

  .story-content h3 {
    font-size:23px;
  }

  .character-container {
    padding:20px;
  }

  .character-top {
    align-items:flex-start;
    flex-direction:column;
    gap:8px;
  }

  .character-grid {
    grid-template-columns:1fr;
    gap:25px;
  }

  .character-photo {
    width:100%;
    max-width:330px;
    height:390px;
    margin:auto;
  }

  .character-name {
    font-size:31px;
  }

  .favorites {
    grid-template-columns:1fr;
  }

  .choice-box {
    padding:40px 20px;
  }

  .choice-box h3 {
    font-size:25px;
  }
}

@media(max-width:380px) {
  nav {
    gap:8px;
  }

  nav a {
    font-size:7px;
  }

  .hero h1 {
    font-size:54px;
  }
}
</style>
</head>

<body>

<div class="bg"></div>
<div class="noise"></div>

<header>
  <div class="brand">♡ SWEET CONFESSION</div>
  <nav>
    <a href="#home">HOME</a>
    <a href="#story">EPISODE</a>
    <a href="#character">CHARACTER</a>
    <a href="#choice">SPECIAL</a>
  </nav>
</header>

<!-- MAIN -->

<main>

<section class="hero" id="home">
  <div class="hero-inner">

    <div class="hero-copy">
      <div class="eyebrow">
        2026. 11. 11 · WEDNESDAY
      </div>

      <h1>
        고백해도
        <span>돼?</span>
      </h1>

      <div class="hero-description">
        11월 11일, 빼빼로 데이.<br>
        오늘은 왠지 평소와 조금 다르다.<br><br>
        <strong>너에게만 전하고 싶은 말이 있거든.</strong>
      </div>

      <button class="enter"
        onclick="document.querySelector('#story').scrollIntoView({behavior:'smooth'})">
        OPEN TODAY'S STORY ↗
      </button>
    </div>

    <div class="hero-art">
      <div class="floating-text ft1">LOVE ♥</div>
      <div class="floating-text ft2">11.11</div>

      <img src="character.png" alt="Character">

      <div class="art-caption">
        PEPERO DAY ♡
      </div>
    </div>

    <div class="hero-number">
      SPECIAL EVENT NO. 0111
    </div>

  </div>
</section>

<!-- STORY -->

<section class="story" id="story">

  <div class="section-head reveal">
    <div class="section-en">TODAY'S EPISODE</div>
    <h2>조금 특별한 하루</h2>
    <p>평범했던 학교생활에 찾아온 작은 변화.</p>
  </div>

  <div class="story-layout reveal">

    <div class="story-side">
      <small>EPISODE 01 / NOVEMBER</small>
      <strong>
        11월 11일.<br>
        너에게 주는<br>
        작은 선물.
      </strong>
      <span>PEPERO DAY · 11:11 AM</span>
    </div>

    <div class="story-content">

      <span class="tag">SCHOOL · ROMANCE</span>

      <h3>
        "야. 이거 네 거."
      </h3>

      <p>
        점심시간이 끝나갈 무렵.

        복도에는 빼빼로를 주고받는 학생들로 가득하다.
        누군가는 친구에게, 누군가는 좋아하는 사람에게.
        
        그렇게 정신없는 와중에 네 앞에 불쑥 나타난 한 사람.

        그는 한 손에 빨간 빼빼로 상자를 들고 있었다.

        "뭘 그렇게 봐?"

        괜히 퉁명스러운 말투.
        그런데 귀 끝은 어쩐지 평소보다 붉다.

        <b>"설마 안 받을 거야?"</b>

        네가 상자를 바라보자 그는 어색하게 시선을 피했다.

        "그냥 남아서 주는 거거든. 착각하지 마."

        ...그런데 왜 굳이 너에게만 주는 걸까?
      </p>

      <div class="story-footer">
        <span>11 : 11 AM</span>
        <span>TO. YOU ♡</span>
      </div>

    </div>

  </div>
</section>

<!-- CHARACTER -->

<section class="character" id="character">

  <div class="section-head reveal">
    <div class="section-en">CHARACTER DATABASE</div>
    <h2>그 애에 대하여</h2>
    <p>오늘 네 앞에 나타난 그 사람.</p>
  </div>

  <div class="character-container reveal">

    <div class="character-top">
      <strong>PROFILE ARCHIVE ♡</strong>
      <span>STUDENT · 2026</span>
    </div>

    <div class="character-grid">

      <div class="character-photo">
        <img src="character.png" alt="Character portrait">
        <div class="photo-label">SPECIAL CHARACTER</div>
      </div>

      <div class="character-info">

        <div class="character-name">
          캐릭터 이름
        </div>

        <div class="character-sub">
          YOUR SPECIAL SOMEONE
        </div>

        <div class="info-row">
          <span>NAME</span>
          <span>캐릭터 이름</span>
        </div>

        <div class="info-row">
          <span>AGE</span>
          <span>00세</span>
        </div>

        <div class="info-row">
          <span>GENDER</span>
          <span>남성</span>
        </div>

        <div class="info-row">
          <span>PERSONALITY</span>
          <span>성격을 입력해 주세요.</span>
        </div>

        <div class="info-row">
          <span>POSITION</span>
          <span>○○고등학교 재학생</span>
        </div>

        <div class="info-row">
          <span>RELATION</span>
          <span>너와의 관계를 입력해 주세요.</span>
        </div>

      </div>
    </div>
  </div>

  <div class="favorites reveal">

    <div class="favorite-card">
      <span>♥ FAVORITE</span>
      <h4>좋아하는 것</h4>
      <p>좋아하는 음식, 취미, 사람 등을 입력해 주세요.</p>
    </div>

    <div class="favorite-card">
      <span>♡ DISLIKE</span>
      <h4>싫어하는 것</h4>
      <p>싫어하는 음식, 행동, 상황 등을 입력해 주세요.</p>
    </div>

  </div>

</section>

<!-- SPECIAL EVENT -->

<section class="choice" id="choice">

  <div class="section-head reveal">
    <div class="section-en">SPECIAL INTERACTION</div>
    <h2>그래서, 받을 거야?</h2>
    <p>그가 건넨 빼빼로. 너의 대답은?</p>
  </div>

  <div class="choice-box reveal">

    <div class="mini">♡ WHAT'S YOUR ANSWER? ♡</div>

    <h3>
      "야, 빨리 대답해 봐."
    </h3>

    <p>
      빼빼로 상자를 내민 채 너를 기다리고 있다.<br>
      괜히 재촉하는 목소리가 조금 떨리는 것 같기도.
    </p>

    <div class="choices">

      <button class="choice-btn"
        onclick="selectAnswer(0)">
        당연히 받을래!
      </button>

      <button class="choice-btn"
        onclick="selectAnswer(1)">
        너도 먹을래?
      </button>

      <button class="choice-btn"
        onclick="selectAnswer(2)">
        왜 나한테 주는데?
      </button>

    </div>

    <div class="answer" id="answer"></div>

  </div>

  <div class="secret reveal">

    <button onclick="secretToggle()">
      ♡ P.S. 그가 숨기고 있는 이야기
    </button>

    <div class="secret-message" id="secret">
      사실은 오늘 아침부터<br>
      너에게 줄 빼빼로를 고르고 있었다.<br><br>
      다른 사람에게는 비밀이야. ♥
    </div>

  </div>

</section>

</main>

<footer>
  <strong>고백해도 돼?</strong>
  A LITTLE SWEET MOMENT WITH YOU.
  <br>
  NOVEMBER 11 · 2026
  <br>
  END OF SPECIAL EVENT
</footer>

<script>

/* ANSWERS */

const responses = [
  "어... 그래. 뭐, 네가 받겠다는데 어쩔 수 없지. <br> (입꼬리가 살짝 올라갔다.)",
  "같이? ...뭐, 그 정도야. <br> (은근슬쩍 네 옆에 자리를 잡는다.)",
  "그냥 주면 안 되냐? <br> ...특별한 이유라도 있어야 돼?"
];

function selectAnswer(index) {
  const answer = document.getElementById('answer');
  answer.innerHTML = responses[index];
  answer.classList.remove('show');

  void answer.offsetWidth;

  answer.classList.add('show');
}

/* SECRET */

function secretToggle() {
  const secret = document.getElementById('secret');
  secret.classList.toggle('show');
}

/* SCROLL REVEAL */

const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if(entry.isIntersecting) {
      entry.target.classList.add('visible');
      observer.unobserve(entry.target);
    }
  });
}, {
  threshold:0.12
});

document.querySelectorAll('.reveal').forEach(el => {
  observer.observe(el);
});

/* ACTIVE NAV */

const sections = document.querySelectorAll('main section[id]');
const navLinks = document.querySelectorAll('nav a');

window.addEventListener('scroll', () => {
  let current = '';

  sections.forEach(section => {
    if(window.scrollY >= section.offsetTop - 150) {
      current = section.id;
    }
  });

  navLinks.forEach(link => {
    link.style.color =
      link.getAttribute('href') === '#' + current
      ? '#ef72ad'
      : '#867586';
  });
});

</script>

</body>
</html>
