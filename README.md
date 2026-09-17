<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Howard Chung — Legal & Management</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Noto+Serif+TC:wght@400;600&display=swap" rel="stylesheet">
  <style>
    /* ===== RESET & BASE ===== */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --bg:       #f5f3f0;
      --surface:  #ffffff;
      --border:   #e2ddd8;
      --ink:      #2a3634;
      --ink2:     #4d5e5c;
      --ink3:     #7a8b89;
      --accent:   #3d5a57;
      --accent-l: #e8efee;
      --shadow:   0 2px 12px rgba(42,54,52,.07);
    }

    html { scroll-behavior: smooth; }

    body {
      background: var(--bg);
      color: var(--ink);
      font-family: 'Inter', 'Noto Serif TC', sans-serif;
      font-size: 17px;
      line-height: 1.85;
      letter-spacing: 0.01em;
      -webkit-font-smoothing: antialiased;
    }

    /* ===== HERO ===== */
    .hero {
      text-align: center;
      padding: 100px 8% 80px;
      background: var(--surface);
      border-bottom: 1px solid var(--border);
    }

    .profile-photo {
      width: 160px;
      height: 160px;
      object-fit: cover;
      border-radius: 10px;
      margin-bottom: 28px;
      border: 3px solid var(--border);
      box-shadow: var(--shadow);
      display: block;
      margin-left: auto;
      margin-right: auto;
    }

    .hero-name {
      font-size: 36px;
      font-weight: 600;
      color: var(--ink);
      margin-bottom: 10px;
      font-family: 'Inter', sans-serif;
    }

    .hero-sub {
      font-size: 16px;
      font-weight: 400;
      color: var(--ink3);
      margin-bottom: 36px;
      letter-spacing: 0.05em;
    }

    .lang-switch {
      display: flex;
      justify-content: center;
      gap: 12px;
    }

    .lang-switch button {
      padding: 10px 28px;
      background: var(--ink);
      color: #fff;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 15px;
      font-family: inherit;
      letter-spacing: 0.03em;
      transition: background 0.2s, transform 0.15s;
    }

    .lang-switch button:hover {
      background: var(--accent);
      transform: translateY(-1px);
    }

    /* ===== CONTENT LAYOUT ===== */
    .content {
      max-width: 820px;
      margin: 0 auto;
      padding: 0 20px 80px;
    }

    /* ===== SECTION CARD ===== */
    .page {
      background: var(--surface);
      border-radius: 14px;
      padding: 52px 56px;
      margin: 32px 0;
      box-shadow: var(--shadow);
      border-left: 4px solid var(--border);
    }

    .page:hover {
      border-left-color: var(--accent);
      transition: border-left-color 0.3s;
    }

    .page h1 {
      font-size: 26px;
      font-weight: 600;
      color: var(--ink);
      margin-bottom: 28px;
      padding-bottom: 16px;
      border-bottom: 1px solid var(--border);
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .page h2 {
      font-size: 18px;
      font-weight: 500;
      color: var(--accent);
      margin: 32px 0 12px;
    }

    .page h3 {
      font-size: 18px;
      font-weight: 600;
      color: var(--ink);
      margin-bottom: 8px;
    }

    .page p {
      color: var(--ink2);
      margin-bottom: 16px;
      max-width: 68ch;
    }

    .page p strong {
      color: var(--ink);
      font-weight: 500;
    }

    .page ul {
      padding-left: 20px;
      color: var(--ink2);
    }

    .page ul li {
      margin-bottom: 10px;
      font-size: 16px;
    }

    /* ===== PHILOSOPHY BLOCK ===== */
    .philosophy-item {
      padding: 16px 20px;
      border-left: 3px solid var(--accent-l);
      margin-bottom: 14px;
      color: var(--ink2);
      font-size: 16px;
      background: var(--bg);
      border-radius: 0 6px 6px 0;
    }

    .philosophy-item strong {
      color: var(--ink);
    }

    /* ===== EXPERIENCE ITEM ===== */
    .exp-item {
      margin-bottom: 40px;
    }

    .exp-item:last-child { margin-bottom: 0; }

    .exp-header {
      display: flex;
      align-items: flex-start;
      gap: 20px;
      margin-bottom: 12px;
    }

    .exp-logo {
      width: 64px;
      height: 64px;
      object-fit: contain;
      border-radius: 8px;
      border: 1px solid var(--border);
      flex-shrink: 0;
    }

    .exp-meta h2 {
      margin: 0 0 4px;
      font-size: 17px;
      font-weight: 600;
      color: var(--ink);
    }

    .exp-period {
      font-size: 13px;
      color: var(--ink3);
      letter-spacing: 0.03em;
    }

    /* ===== SHOWCASE CARD ===== */
    .showcase-card {
      display: flex;
      gap: 24px;
      align-items: flex-start;
      margin: 28px 0;
      padding: 24px;
      background: var(--bg);
      border-radius: 10px;
      border: 1px solid var(--border);
    }

    .system-img {
      width: 140px;
      height: 140px;
      object-fit: contain;
      border-radius: 8px;
      border: 1px solid var(--border);
      background: #fff;
      flex-shrink: 0;
      cursor: zoom-in;
      transition: transform 0.22s ease, box-shadow 0.22s ease;
    }

    .system-img:hover {
      transform: scale(1.06);
      box-shadow: 0 6px 20px rgba(42,54,52,.15);
    }

    .showcase-text h3 {
      font-size: 17px;
      font-weight: 600;
      color: var(--ink);
      margin-bottom: 8px;
    }

    .showcase-text p {
      font-size: 15px;
      color: var(--ink3);
      margin: 0;
      max-width: 52ch;
    }

    /* ===== DOWNLOAD BUTTONS ===== */
    .download-box {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
      margin-top: 8px;
    }

    .download-btn {
      display: inline-block;
      padding: 12px 26px;
      background: var(--ink);
      color: #fff;
      border-radius: 8px;
      text-decoration: none;
      font-size: 15px;
      letter-spacing: 0.02em;
      transition: background 0.2s, transform 0.15s;
      box-shadow: var(--shadow);
    }

    .download-btn:hover {
      background: var(--accent);
      transform: translateY(-1px);
      color: #fff;
    }

    /* ===== LIGHTBOX ===== */
    .lightbox {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.88);
      justify-content: center;
      align-items: center;
      z-index: 9999;
      cursor: zoom-out;
    }

    .lightbox.open { display: flex; }

    .lightbox img {
      max-width: 92vw;
      max-height: 92vh;
      width: auto;
      height: auto;
      border-radius: 10px;
      box-shadow: 0 8px 40px rgba(0,0,0,0.5);
      animation: lbIn 0.18s ease;
    }

    @keyframes lbIn {
      from { transform: scale(0.88); opacity: 0; }
      to   { transform: scale(1);    opacity: 1; }
    }

    .lightbox-close {
      position: absolute;
      top: 20px;
      right: 24px;
      color: rgba(255,255,255,0.7);
      font-size: 28px;
      cursor: pointer;
      line-height: 1;
      user-select: none;
    }

    .lightbox-close:hover { color: #fff; }

    /* ===== LINKS ===== */
    a { color: var(--accent); text-decoration: none; }
    a:hover { text-decoration: underline; }

    /* ===== SKILL GRID ===== */
    .skill-group {
      margin-bottom: 28px;
    }

    /* ===== RESPONSIVE ===== */
    @media (max-width: 640px) {
      .hero { padding: 72px 6% 60px; }
      .hero-name { font-size: 28px; }
      .page { padding: 36px 28px; }
      .showcase-card { flex-direction: column; }
      .system-img { width: 100%; height: 200px; }
      .exp-header { flex-direction: column; gap: 12px; }
      .download-box { flex-direction: column; }
      .download-btn { text-align: center; }
    }

    @media (prefers-reduced-motion: reduce) {
      * { animation: none !important; transition: none !important; }
    }
  </style>
</head>

<body>

<!-- ===== HERO ===== -->
<header class="hero">
  <img src="https://i.postimg.cc/hjvFH4SW/zi-pai.png" class="profile-photo" alt="Howard Chung">
  <h1 class="hero-name">Howard (昊恩) Chung</h1>
  <p class="hero-sub"> Legal Innovation · Tech Systems · Organizational Management </p>
  <div class="lang-switch">
    <button onclick="showZH()" aria-label="切換中文">中文</button>
    <button onclick="showEN()" aria-label="Switch to English">English</button>
  </div>
</header>

<!-- ===== 中文內容 ===== -->
<div id="zh">
<main class="content">

  <section class="page">
    <h1>關於我</h1>
    <p>
      我是鍾昊恩，一位結合法務、組織治理與系統設計的跨領域整合者。
      我相信法律不只是風險控管，而是能夠讓組織更聰明、更高效的「結構設計工具」。
    </p>
    <p>
      在過去的職涯中，我從法律專業出發，逐步擴展到流程優化、跨部門協作、治理架構設計與 LegalTech 系統開發，並在不同產業中打造能真正落地的管理機制。
    </p>
    <p>
      我擅長將複雜問題拆解成可執行的流程，並以系統化方式提升組織的透明度、效率與決策品質。
    </p>
    <p><strong>我的工作理念：讓組織運作更順暢，讓人能專注在真正重要的事。</strong></p>
  </section>

  <section class="page">
    <h1>核心經歷</h1>
    <ul>
      <li>建立完整法務管理系統以大幅提高效率（合約、授權、風控、治理）</li>
      <li>主導跨部門治理架構（法務 × 行銷 × 產品 × 動畫 × 商務）</li>
      <li>設計動畫 IP 授權流程與風控機制</li>
      <li>建立跨國合規流程（台灣 × 中國 × 東南亞）</li>
      <li>開發 LegalTech 工具提升透明度與追蹤效率</li>
      <li>協助公司完成重大商務協議與策略合作</li>
    </ul>
  </section>

  <section class="page">
    <h1>專業理念</h1>
    <div class="philosophy-item"><strong>法律應該是組織的結構，而不是阻力。</strong></div>
    <div class="philosophy-item"><strong>好的流程能減少摩擦；好的系統能創造清晰。</strong></div>
    <div class="philosophy-item"><strong>治理不是管控，而是讓每個人都能更好地完成工作。</strong></div>
    <div class="philosophy-item"><strong>法務的價值在於讓組織更聰明，而不是更複雜。</strong></div>
  </section>

  <section class="page">
    <h1>技能專長</h1>
    <div class="skill-group">
      <h2>法律技能</h2>
      <ul>
        <li>智財、民事、刑事案件分析與處理</li>
        <li>消費爭議與商業談判</li>
        <li>中英文契約擬定與審閱</li>
        <li>商標申請與函文撰擬</li>
        <li>內部流程規劃與管理</li>
        <li>跨境法律事務與談判</li>
      </ul>
    </div>
    <div class="skill-group">
      <h2>管理技能</h2>
      <ul>
        <li>KPI/OKR 設計與法務產值化</li>
        <li>職能盤點、人才評鑑與培訓規劃</li>
        <li>部門制度建置與治理框架設計</li>
        <li>跨境法務執行能力建立</li>
        <li>總務預算管理與組織文化重塑</li>
      </ul>
    </div>
  </section>

  <section class="page">
    <h1>工作經歷</h1>

    <div class="exp-item">
      <div class="exp-header">
        <img class="exp-logo" src="https://i.postimg.cc/gxsp40TZ/Copilot-20260907-180619.png" alt="電商公司">
        <div class="exp-meta">
          <h2>電子商務公司｜法務主任</h2>
          <span class="exp-period">2014 – 2020</span>
        </div>
      </div>
      <p>
        公司首任法務，參與興櫃、上櫃、子公司設立等重大事件。負責契約審閱、制度建置、消費爭議、交易安全、智財維護與主管機關溝通。
      </p>
    </div>

    <div class="exp-item">
      <div class="exp-header">
        <img class="exp-logo" src="https://i.postimg.cc/4YPGw3Sh/Copilot-20260907-180609.png" alt="IP動畫公司">
        <div class="exp-meta">
          <h2>IP 動畫代理公司｜資深法務經理 → 管理處代理處長</h2>
          <span class="exp-period">2020 – 2026</span>
        </div>
      </div>
      <p>
        建立法務部門並擴張職責至兼管總務與人資，統籌三部門。處理跨境授權、代理、合約執行，建立 KPI/OKR、職能盤點、跨境法務能力、商標策略與集團治理藍圖。
      </p>
    </div>
  </section>

  <section class="page">
    <h1>作品展示</h1>
    <h2>LegalTech 系統展示</h2>

    <div class="showcase-card">
      <img class="system-img"
           src="https://i.postimg.cc/yJNHGzMk/Copilot-20260907-180622.png"
           alt="法務產值管理系統"
           onclick="showLightbox('https://i.postimg.cc/yJNHGzMk/Copilot-20260907-180622.png')">
      <div class="showcase-text">
        <h3>法務產值管理系統</h3>
        <p>
          整合法務案件、工作紀錄與人員資料，量化團隊工作成果與貢獻，支援資源配置與管理決策。
        </p>
      </div>
    </div>

    <div class="showcase-card">
      <img class="system-img"
           src="https://i.postimg.cc/tskbDgMq/Copilot-20260907-180625.png"
           alt="法務專案與職能培養系統"
           onclick="showLightbox('https://i.postimg.cc/tskbDgMq/Copilot-20260907-180625.png')">
      <div class="showcase-text">
        <h3>法務專案與職能培養系統</h3>
        <p>
          管理 Project、Case、OKR 與人員配置，提供進度追蹤與協作治理，強化專案執行能見度與人才培養。
        </p>
      </div>
    </div>
  </section>

  <section class="page">
    <h1>履歷</h1>
    <div class="download-box">
      <a class="download-btn" href="https://drive.google.com/uc?export=download&id=1sUDMzLEmnhsE82RpBMcO15OghHo_QU3V" target="_blank" rel="noopener">
        下載中文履歷 PDF
      </a>
      <a class="download-btn" href="https://drive.google.com/uc?export=download&id=1U8Hg6XkHCQOtnHV5AVGtmDdrkE5t4N7c" target="_blank" rel="noopener">
        下載英文履歷 PDF
      </a>
    </div>
  </section>

  <section class="download-section">
  <h2>下載專區</h2>

  <div class="download-box">
    <a class="download-btn" href="https://drive.google.com/uc?export=download&id=1UjL9k6nadRY3zHwbiU-YwLNSB37xjiFD" target="_blank">下載 CV</a>
    <a class="download-btn" href="https://docs.google.com/presentation/d/1QG_DDAcJgzeLgZLJUs0GU5RKogXh4w4l/edit?usp=sharing&ouid=115455907322270686316&rtpof=true&sd=true" target="_blank">下載作品集</a>
  </div>
</section>


</main>
</div>


<!-- ===== English Content ===== -->
<div id="en" style="display:none;">
<main class="content">

  <section class="page">
    <h1>About Me</h1>
    <p>
      I'm Howard, a cross-disciplinary integrator combining legal expertise, organizational governance, and system design. I believe legal work is not merely risk control — it is a structural tool that makes organizations smarter and more efficient.
    </p>
    <p>
      I specialize in transforming complex problems into actionable processes that enhance clarity, efficiency, and decision-making quality.
    </p>
    <p><strong>My mission: build systems that reduce friction and allow people to focus on what truly matters.</strong></p>
  </section>

  <section class="page">
    <h1>Core Experience</h1>
    <ul>
      <li>Built a full legal management system (contracts, licensing, risk, governance)</li>
      <li>Led cross-functional governance across Legal, Marketing, Product, Animation, and Business</li>
      <li>Designed IP licensing workflows and risk controls for animation projects</li>
      <li>Established cross-border compliance processes (Taiwan × China × Southeast Asia)</li>
      <li>Developed LegalTech tools improving transparency and tracking efficiency</li>
      <li>Supported major commercial agreements and strategic partnerships</li>
    </ul>
  </section>

  <section class="page">
    <h1>Professional Philosophy</h1>
    <div class="philosophy-item"><strong>Legal should be a structure, not a barrier.</strong></div>
    <div class="philosophy-item"><strong>A good process reduces friction; a great system creates clarity.</strong></div>
    <div class="philosophy-item"><strong>Governance is not control — it's enabling people to do their best work.</strong></div>
    <div class="philosophy-item"><strong>The value of legal is making the organization smarter, not more complicated.</strong></div>
  </section>

  <section class="page">
    <h1>Skills</h1>
    <div class="skill-group">
      <h2>Legal Skills</h2>
      <ul>
        <li>IP, civil, and criminal case analysis</li>
        <li>Consumer dispute consultation and negotiation</li>
        <li>Bilingual contract drafting and review</li>
        <li>Trademark application and official correspondence</li>
        <li>Internal process planning and management</li>
        <li>Cross-border legal affairs and negotiation</li>
      </ul>
    </div>
    <div class="skill-group">
      <h2>Management Skills</h2>
      <ul>
        <li>KPI/OKR design and legal output monetization</li>
        <li>Competency mapping, talent evaluation, and training</li>
        <li>Governance framework and system building</li>
        <li>Cross-border execution capability development</li>
        <li>Budget management and organizational culture shaping</li>
      </ul>
    </div>
  </section>

  <section class="page">
    <h1>Professional Experience</h1>

    <div class="exp-item">
      <div class="exp-header">
        <img class="exp-logo" src="https://i.postimg.cc/gxsp40TZ/Copilot-20260907-180619.png" alt="E-Commerce Company">
        <div class="exp-meta">
          <h2>E-Commerce Company | Legal Director</h2>
          <span class="exp-period">2014 – 2020</span>
        </div>
      </div>
      <p>
        First and sole legal professional, contributing to Emerging Stock and TPEx listings. Responsible for contract review, compliance frameworks, consumer protection, IP maintenance, and regulatory communication.
      </p>
    </div>

    <div class="exp-item">
      <div class="exp-header">
        <img class="exp-logo" src="https://i.postimg.cc/4YPGw3Sh/Copilot-20260907-180609.png" alt="IP Animation Company">
        <div class="exp-meta">
          <h2>IP Animation Licensing Company | Legal Senior Manager → Acting Division Supervisor</h2>
          <span class="exp-period">2020 – 2026</span>
        </div>
      </div>
      <p>
        Led Legal, HR, and GA teams. Managed cross-border licensing, KPI/OKR implementation, competency mapping, trademark strategy, and group governance blueprint development.
      </p>
    </div>
  </section>

  <section class="page">
    <h1>Showcase</h1>
    <h2>LegalTech Systems</h2>

    <div class="showcase-card">
      <img class="system-img"
           src="https://i.postimg.cc/yJNHGzMk/Copilot-20260907-180622.png"
           alt="Legal Productivity Management System"
           onclick="showLightbox('https://i.postimg.cc/yJNHGzMk/Copilot-20260907-180622.png')">
      <div class="showcase-text">
        <h3>Legal Productivity Management System</h3>
        <p>
          Integrates cases, work logs, and personnel data to quantify team output and support resource allocation and management decisions.
        </p>
      </div>
    </div>

    <div class="showcase-card">
      <img class="system-img"
           src="https://i.postimg.cc/tskbDgMq/Copilot-20260907-180625.png"
           alt="Legal Project & Competency Development System"
           onclick="showLightbox('https://i.postimg.cc/tskbDgMq/Copilot-20260907-180625.png')">
      <div class="showcase-text">
        <h3>Legal Project &amp; Competency Development System</h3>
        <p>
          Manages projects, cases, OKRs, and personnel allocation, providing visibility into execution and competency development.
        </p>
      </div>
    </div>
  </section>

  <section class="page">
    <h1>Resume</h1>
    <div class="download-box">
      <a class="download-btn" href="https://drive.google.com/uc?export=download&id=1sUDMzLEmnhsE82RpBMcO15OghHo_QU3V" target="_blank" rel="noopener">
        Download Chinese Resume PDF
      </a>
      <a class="download-btn" href="https://drive.google.com/uc?export=download&id=1U8Hg6XkHCQOtnHV5AVGtmDdrkE5t4N7c" target="_blank" rel="noopener">
        Download English Resume PDF
      </a>
    </div>
  </section>

  <section class="download-section">
  <h2>Downloads</h2>

  <div class="download-box">
    <a class="download-btn" href="https://drive.google.com/uc?export=download&id=1UjL9k6nadRY3zHwbiU-YwLNSB37xjiFD" target="_blank">Download CV</a>
    <a class="download-btn" href="https://docs.google.com/presentation/d/1QG_DDAcJgzeLgZLJUs0GU5RKogXh4w4l/edit?usp=sharing&ouid=115455907322270686316&rtpof=true&sd=true" target="_blank">Download Portfolio</a>
  </div>
</section>


</main>
</div>


<!-- ===== LIGHTBOX ===== -->
<div id="lightbox" class="lightbox" role="dialog" aria-modal="true" aria-label="圖片放大">
  <span class="lightbox-close" onclick="closeLightbox()" aria-label="關閉">✕</span>
  <img id="lightbox-img" src="" alt="放大圖片">
</div>


<!-- ===== SCRIPTS ===== -->
<script>
  function showZH() {
    document.getElementById('zh').style.display = 'block';
    document.getElementById('en').style.display = 'none';
  }

  function showEN() {
    document.getElementById('zh').style.display = 'none';
    document.getElementById('en').style.display = 'block';
  }

  function showLightbox(src) {
    const lb = document.getElementById('lightbox');
    document.getElementById('lightbox-img').src = src;
    lb.classList.add('open');
    document.body.style.overflow = 'hidden';
  }

  function closeLightbox() {
    document.getElementById('lightbox').classList.remove('open');
    document.body.style.overflow = '';
  }

  document.getElementById('lightbox').addEventListener('click', function(e) {
    if (e.target === this || e.target === document.getElementById('lightbox-img')) {
      closeLightbox();
    }
  });

  document.addEventListener('keydown', function(e) {
    if (e.key === 'Escape') closeLightbox();
  });
</script>

</body>
</html>
