# 오픈소스 기말프로젝트
오픈소스 기말프로젝트
<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>프로토타입 홈페이지 — Cherish</title>
  <style>
    :root{
      --bg:#0f1724; --card:#0b1220; --muted:#9aa4b2; --accent:#4f46e5;
      --glass: rgba(255,255,255,0.04);
      color-scheme: dark;
    }
    *{box-sizing:border-box}
    body{
      margin:0; font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background: linear-gradient(180deg,#071029 0%, #071523 100%); color:#e6eef8; line-height:1.5;
    }
    header{
      display:flex; align-items:center; justify-content:space-between;
      padding:18px 24px; backdrop-filter: blur(6px);
    }
    .brand{display:flex; gap:12px; align-items:center;}
    .logo{
      width:44px; height:44px; border-radius:10px;
      background:linear-gradient(135deg,#7c3aed,#06b6d4); display:inline-flex; align-items:center; justify-content:center;
      font-weight:700; font-size:18px; color:white;
    }
    nav{display:flex; gap:12px; align-items:center;}
    nav a{color:var(--muted); text-decoration:none; padding:6px 10px; border-radius:8px; font-size:15px;}
    nav a:hover{background:var(--glass); color:#fff}
    .btn-primary{
      background:var(--accent); color:white; padding:8px 12px; border-radius:10px; text-decoration:none; font-weight:600;
    }

    main{padding:28px 24px; max-width:1100px; margin:0 auto;}
    .hero{
      display:grid; grid-template-columns:1fr 360px; gap:24px; align-items:center; margin-top:22px;
    }
    .hero .card{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      padding:28px; border-radius:14px; box-shadow: 0 6px 18px rgba(2,6,23,0.6);
    }
    h1{margin:0 0 10px 0; font-size:30px}
    p.lead{color:var(--muted); margin:0 0 16px 0}
    .features{display:flex; gap:12px; flex-wrap:wrap; margin-top:14px}
    .feature{
      background:rgba(255,255,255,0.02); padding:12px 14px; border-radius:10px; font-size:14px; color:var(--muted);
    }

    .card-aside{
      display:flex; flex-direction:column; gap:12px;
    }
    .profile{
      display:flex; gap:12px; align-items:center;
    }
    .avatar{width:66px; height:66px; border-radius:12px; background:linear-gradient(135deg,#06b6d4,#7c3aed)}
    .small{font-size:13px; color:var(--muted)}

    section.gallery{margin-top:26px;}
    .grid{
      display:grid; grid-template-columns:repeat(3,1fr); gap:14px;
    }
    .tile{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      padding:18px; border-radius:12px; min-height:110px;
    }
    .cta{
      margin-top:24px; display:flex; gap:12px; align-items:center;
    }

    footer{margin-top:32px; padding:20px 0; text-align:center; color:var(--muted); font-size:14px;}

    /* responsive */
    @media(max-width:900px){
      .hero{grid-template-columns:1fr; }
      .grid{grid-template-columns:repeat(2,1fr)}
    }
    @media(max-width:520px){
      nav{display:none}
      .grid{grid-template-columns:1fr}
      header{padding:14px}
    }
    /* simple form styles */
    form input, form textarea{
      width:100%; padding:10px 12px; border-radius:8px; border:1px solid rgba(255,255,255,0.04);
      background:transparent; color:inherit; margin-bottom:10px;
    }
    .theme-toggle{background:transparent; color:var(--muted); border:1px solid rgba(255,255,255,0.03); padding:8px 10px; border-radius:8px}
  </style>
</head>
<body>
  <header>
    <div class="brand">
      <div class="logo">CJ</div>
      <div>
        <div style="font-weight:700">Cherish Prototype</div>
        <div style="font-size:13px;color:var(--muted)">간단한 포트폴리오/랜딩 프로토타입</div>
      </div>
    </div>

    <nav aria-label="주요">
      <a href="#home">홈</a>
      <a href="#works">작업</a>
      <a href="#about">소개</a>
      <a href="#contact" class="btn-primary">연락하기</a>
    </nav>

    <div style="display:flex; gap:8px; align-items:center">
      <button class="theme-toggle" id="toggleTheme">theme</button>
    </div>
  </header>

  <main>
    <section class="hero">
      <div class="card">
        <h1 id="home">안녕하세요, 저는 Cherish입니다.</h1>
        <p class="lead">웹/프론트엔드 프로토타입과 간단한 포트폴리오 페이지 예시입니다. 필요하신 스타일이나 기능을 알려주세요.</p>

        <div class="features">
          <div class="feature">반응형 디자인</div>
          <div class="feature">간단한 포트폴리오 그리드</div>
          <div class="feature">연락처 폼 (프론트엔드)</div>
        </div>

        <div class="cta">
          <a href="#works" class="btn-primary">작업 보기</a>
          <a href="#contact" style="color:var(--muted); text-decoration:none; padding:8px 10px; border-radius:8px">더 알아보기</a>
        </div>
      </div>

      <aside class="card card-aside">
        <div class="profile">
          <div class="avatar"></div>
          <div>
            <div style="font-weight:700">Cherish J</div>
            <div class="small">Frontend Developer · Prototype</div>
          </div>
        </div>

        <div style="font-size:13px; color:var(--muted)">
          간단한 소개 텍스트를 넣을 수 있습니다. 깔끔하고 빠르게 배포 가능한 정적 페이지입니다.
        </div>

        <div style="margin-top:auto">
          <div style="font-size:13px; color:var(--muted); margin-bottom:8px">최근 연락처</div>
          <div style="display:flex; gap:8px">
            <a class="btn-primary" href="mailto:hello@example.com">이메일</a>
            <a style="padding:8px 10px; border-radius:8px; color:var(--muted); background:transparent; text-decoration:none" href="#">깃허브</a>
          </div>
        </div>
      </aside>
    </section>

    <section class="gallery" id="works">
      <h2 style="margin:18px 0 12px 0">작업 샘플</h2>
      <div class="grid">
        <div class="tile"><strong>프로젝트 A</strong><div class="small" style="margin-top:8px">간단한 랜딩 페이지 디자인.</div></div>
        <div class="tile"><strong>프로젝트 B</strong><div class="small" style="margin-top:8px">대시보드 UI 컴포넌트 라이브러리.</div></div>
        <div class="tile"><strong>프로젝트 C</strong><div class="small" style="margin-top:8px">포트폴리오 사이트 전체 구축.</div></div>
        <div class="tile"><strong>프로젝트 D</strong><div class="small" style="margin-top:8px">작은 인터랙션 실험.</div></div>
        <div class="tile"><strong>프로젝트 E</strong><div class="small" style="margin-top:8px">반응형 그리드 구현.</div></div>
        <div class="tile"><strong>프로젝트 F</strong><div class="small" style="margin-top:8px">접근성 개선 예시.</div></div>
      </div>
    </section>

    <section id="about" style="margin-top:28px">
      <h2>소개</h2>
      <p class="small" style="max-width:720px">이 템플릿은 빠른 프로토타입 제작용으로 설계되었습니다. HTML 하나로 구조, CSS로 스타일, 약간의 JS로 토글 및 폼 동작을 포함합니다. 필요하면 React/Next로 변환해 드립니다.</p>
    </section>

    <section id="contact" style="margin-top:20px">
      <h2>연락</h2>
      <form onsubmit="handleSubmit(event)" style="max-width:720px" novalidate>
        <input type="text" id="name" placeholder="이름" required />
        <input type="email" id="email" placeholder="이메일" required />
        <textarea id="message" placeholder="메시지" rows="5" required></textarea>
        <div style="display:flex; gap:8px; align-items:center">
          <button type="submit" class="btn-primary">전송 (데모)</button>
          <div class="small" id="formStatus" style="color:var(--muted)"></div>
        </div>
      </form>
    </section>

    <footer>
      © <span id="year"></span> Cherish Prototype · 간단한 데모 페이지
    </footer>
  </main>

  <script>
    // small interactive bits
    document.getElementById('year').textContent = new Date().getFullYear();

    document.getElementById('toggleTheme').addEventListener('click', () => {
      const root = document.documentElement;
      if (root.style.getPropertyValue('--bg') === '#0f1724') {
        // light-ish
        root.style.setProperty('--bg','#f7f9fc');
        root.style.setProperty('--card','#ffffff');
        root.style.setProperty('--muted','#6b7280');
        root.style.setProperty('--accent','#2563eb');
        document.body.style.background = 'linear-gradient(180deg,#fbfdff,#eef2ff)';
        document.body.style.color = '#071426';
      } else {
        root.style.setProperty('--bg','#0f1724');
        root.style.setProperty('--card','#0b1220');
        root.style.setProperty('--muted','#9aa4b2');
        root.style.setProperty('--accent','#4f46e5');
        document.body.style.background = 'linear-gradient(180deg,#071029,#071523)';
        document.body.style.color = '#e6eef8';
      }
    });

    function handleSubmit(e){
      e.preventDefault();
      const name = document.getElementById('name').value.trim();
      const email = document.getElementById('email').value.trim();
      const msg = document.getElementById('message').value.trim();
      const status = document.getElementById('formStatus');
      if(!name || !email || !msg){ status.textContent = '모든 필드를 입력해주세요.'; return; }
      // 데모: 실제 전송 없음
      status.textContent = '메시지 전송(데모): 성공! 감사합니다.';
      // 리셋 폼
      e.target.reset();
      setTimeout(()=> status.textContent = '', 4000);
    }
  </script>
</body>
</html>
