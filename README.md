
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="だるま工房 吉んと — 吉(良きこと)がうんと(たくさん)ありますように。群馬発、心を込めて仕上げた縁起だるまのオンラインストア。">
  <title>だるま工房 吉んと</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Noto+Serif+JP:wght@400;700&family=Noto+Sans+JP:wght@300;400;500&display=swap" rel="stylesheet">
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --red:       #c0392b;
      --red-deep:  #8f3418;
      --red-light: #d44e3a;
      --gold:      #c8a050;
      --gold-pale: #e8d8b8;
      --brown:     #2a1a0a;
      --brown-mid: #5a4a3a;
      --brown-lt:  #7a6a5a;
      --cream:     #faf8f3;
      --cream-dk:  #f5efe4;
      --border:    #e0d4c0;
      --border-lt: #f0e8d8;
      --white:     #ffffff;
    }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'Noto Sans JP', sans-serif;
      color: var(--brown);
      background: var(--cream);
      min-height: 100vh;
      font-size: 16px;
      line-height: 1.7;
    }

    /* ===== NAV ===== */
    nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 14px 40px;
      background: var(--white);
      border-bottom: 1px solid var(--border);
      position: sticky;
      top: 0;
      z-index: 200;
    }

    .nav-logo {
      font-family: 'Noto Serif JP', serif;
      font-size: 15px;
      font-weight: 700;
      color: var(--brown);
      letter-spacing: 0.08em;
      line-height: 1.3;
      text-decoration: none;
    }
    .nav-logo span {
      display: block;
      font-family: 'Noto Sans JP', sans-serif;
      font-size: 10px;
      font-weight: 300;
      color: var(--brown-lt);
      letter-spacing: 0.2em;
      margin-top: 2px;
    }

    .nav-links {
      display: flex;
      gap: 28px;
      list-style: none;
    }
    .nav-links a {
      font-size: 12px;
      color: var(--brown-mid);
      text-decoration: none;
      letter-spacing: 0.1em;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--red); }

    .nav-right {
      display: flex;
      align-items: center;
      gap: 20px;
    }
    .nav-sns {
      display: flex;
      gap: 12px;
    }
    .nav-sns a {
      color: var(--brown-lt);
      transition: color 0.2s;
    }
    .nav-sns a:hover { color: var(--red); }
    .nav-cart {
      font-size: 11px;
      color: var(--red);
      text-decoration: none;
      border: 1px solid var(--red);
      padding: 5px 16px;
      border-radius: 2px;
      letter-spacing: 0.05em;
      transition: background 0.2s, color 0.2s;
    }
    .nav-cart:hover { background: var(--red); color: var(--white); }

    .nav-hamburger {
      display: none;
      background: none;
      border: none;
      cursor: pointer;
      padding: 4px;
      color: var(--brown);
    }

    /* ===== HERO ===== */
    .hero {
      position: relative;
      background: var(--brown);
      height: 520px;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .hero-pattern {
      position: absolute;
      inset: 0;
      opacity: 0.06;
      background-image:
        repeating-linear-gradient(45deg, #c8a050 0, #c8a050 1px, transparent 0, transparent 50%);
      background-size: 20px 20px;
    }

    .hero-daruma {
      position: absolute;
      right: 12%;
      bottom: 0;
      opacity: 0.18;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      text-align: center;
      color: var(--white);
      padding: 0 24px;
    }
    .hero-eyebrow {
      font-size: 11px;
      letter-spacing: 0.4em;
      color: var(--gold);
      margin-bottom: 20px;
    }
    .hero-title {
      font-family: 'Noto Serif JP', serif;
      font-size: 40px;
      font-weight: 700;
      letter-spacing: 0.12em;
      line-height: 1.5;
      margin-bottom: 20px;
    }
    .hero-title em {
      font-style: normal;
      color: #e8a050;
    }
    .hero-sub {
      font-size: 13px;
      color: #c0b09a;
      letter-spacing: 0.1em;
      line-height: 2.2;
      margin-bottom: 36px;
    }
    .hero-cta {
      display: inline-block;
      background: var(--red);
      color: var(--white);
      text-decoration: none;
      padding: 14px 44px;
      font-size: 13px;
      letter-spacing: 0.2em;
      border-radius: 2px;
      transition: background 0.2s, transform 0.15s;
    }
    .hero-cta:hover { background: var(--red-deep); transform: translateY(-1px); }

    /* ===== SECTION COMMON ===== */
    .section-label {
      font-size: 10px;
      letter-spacing: 0.4em;
      color: var(--red);
      text-transform: uppercase;
      margin-bottom: 12px;
    }
    .section-title {
      font-family: 'Noto Serif JP', serif;
      font-size: 24px;
      font-weight: 700;
      color: var(--brown);
      letter-spacing: 0.1em;
    }
    .section-header { text-align: center; margin-bottom: 48px; }

    .divider {
      display: flex;
      align-items: center;
      gap: 16px;
      padding: 0 40px;
      margin: 0;
    }
    .divider-line { flex: 1; height: 1px; background: var(--border); }
    .divider-mark { color: var(--gold); font-size: 12px; letter-spacing: 4px; }

    /* ===== GREETING ===== */
    .greeting {
      padding: 80px 40px;
      max-width: 680px;
      margin: 0 auto;
      text-align: center;
    }
    .greeting-title {
      font-family: 'Noto Serif JP', serif;
      font-size: 20px;
      font-weight: 700;
      color: var(--brown);
      line-height: 1.9;
      margin-bottom: 28px;
      letter-spacing: 0.06em;
    }
    .greeting-body {
      font-size: 14px;
      line-height: 2.2;
      color: var(--brown-mid);
      letter-spacing: 0.05em;
    }

    /* ===== FEATURE CARDS ===== */
    .features {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      border-top: 1px solid var(--border);
      border-bottom: 1px solid var(--border);
    }
    .feat-card {
      padding: 56px 32px;
      text-align: center;
      border-right: 1px solid var(--border);
      background: var(--white);
      cursor: pointer;
      transition: background 0.2s;
      text-decoration: none;
      color: inherit;
      display: block;
    }
    .feat-card:last-child { border-right: none; }
    .feat-card:hover { background: #fdf5ec; }
    .feat-icon {
      width: 72px;
      height: 72px;
      margin: 0 auto 20px;
    }
    .feat-title {
      font-family: 'Noto Serif JP', serif;
      font-size: 15px;
      font-weight: 700;
      color: var(--brown);
      margin-bottom: 12px;
      letter-spacing: 0.08em;
    }
    .feat-desc {
      font-size: 12px;
      color: var(--brown-lt);
      line-height: 2.0;
      letter-spacing: 0.04em;
    }

    /* ===== PRODUCTS ===== */
    .products {
      padding: 80px 40px;
      background: var(--cream);
    }
    .product-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      gap: 20px;
      max-width: 900px;
      margin: 0 auto;
    }
    .product-card {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: 4px;
      overflow: hidden;
      cursor: pointer;
      transition: transform 0.18s, box-shadow 0.18s;
      text-decoration: none;
      color: inherit;
      display: block;
    }
    .product-card:hover {
      transform: translateY(-3px);
      box-shadow: 0 8px 24px rgba(42,26,10,0.1);
    }
    .product-img {
      height: 140px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: var(--cream-dk);
    }
    .product-info { padding: 16px; }
    .product-name {
      font-size: 13px;
      font-weight: 500;
      color: var(--brown);
      letter-spacing: 0.06em;
      margin-bottom: 4px;
    }
    .product-tag {
      font-size: 11px;
      color: var(--red);
      letter-spacing: 0.05em;
    }

    /* ===== NEWS ===== */
    .news {
      padding: 72px 40px;
      background: var(--white);
      border-top: 1px solid var(--border);
    }
    .news-list {
      max-width: 600px;
      margin: 0 auto;
    }
    .news-item {
      display: flex;
      gap: 24px;
      align-items: flex-start;
      padding: 18px 0;
      border-bottom: 1px solid var(--border-lt);
    }
    .news-date {
      font-size: 11px;
      color: #8a7a6a;
      white-space: nowrap;
      letter-spacing: 0.05em;
      padding-top: 2px;
    }
    .news-link {
      font-size: 13px;
      color: var(--brown);
      text-decoration: none;
      letter-spacing: 0.04em;
      line-height: 1.7;
      transition: color 0.2s;
    }
    .news-link:hover { color: var(--red); }
    .news-more {
      display: block;
      text-align: center;
      margin-top: 28px;
      font-size: 12px;
      color: var(--red);
      text-decoration: none;
      letter-spacing: 0.15em;
      border: 1px solid var(--red);
      padding: 10px 32px;
      border-radius: 2px;
      width: fit-content;
      margin-left: auto;
      margin-right: auto;
      transition: background 0.2s, color 0.2s;
    }
    .news-more:hover { background: var(--red); color: var(--white); }

    /* ===== CALENDAR ===== */
    .calendar-section {
      padding: 72px 40px;
      background: var(--cream);
      border-top: 1px solid var(--border);
    }
    .calendar-wrap {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 32px;
      max-width: 700px;
      margin: 0 auto;
    }
    .cal-block h3 {
      font-family: 'Noto Serif JP', serif;
      font-size: 14px;
      font-weight: 700;
      color: var(--brown);
      margin-bottom: 12px;
      letter-spacing: 0.05em;
    }
    .cal-table {
      width: 100%;
      border-collapse: collapse;
      font-size: 12px;
    }
    .cal-table th {
      color: var(--brown-lt);
      font-weight: 400;
      text-align: center;
      padding: 4px 0;
      border-bottom: 1px solid var(--border);
      letter-spacing: 0.05em;
    }
    .cal-table th.sun { color: #c0392b; }
    .cal-table th.sat { color: #2060a0; }
    .cal-table td {
      text-align: center;
      padding: 5px 2px;
      color: var(--brown-mid);
    }
    .cal-table td.sun { color: #c0392b; }
    .cal-table td.sat { color: #2060a0; }
    .cal-table td.today {
      background: var(--red);
      color: var(--white);
      border-radius: 50%;
      font-weight: 500;
    }
    .cal-legend {
      display: flex;
      align-items: center;
      gap: 8px;
      margin-top: 10px;
      font-size: 11px;
      color: var(--brown-lt);
    }
    .cal-legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: #ddd;
      display: inline-block;
    }

    /* ===== SNS BAR ===== */
    .sns-bar {
      background: var(--brown);
      padding: 28px 40px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 40px;
    }
    .sns-label {
      font-size: 10px;
      color: var(--gold);
      letter-spacing: 0.35em;
      text-transform: uppercase;
    }
    .sns-link {
      display: flex;
      align-items: center;
      gap: 8px;
      text-decoration: none;
      color: var(--gold-pale);
      font-size: 12px;
      letter-spacing: 0.1em;
      transition: color 0.2s;
    }
    .sns-link:hover { color: var(--gold); }
    .sns-link svg { flex-shrink: 0; }

    /* ===== FOOTER ===== */
    footer {
      background: #140b03;
      padding: 48px 40px;
      text-align: center;
      color: #7a6050;
      font-size: 11px;
      letter-spacing: 0.1em;
      line-height: 2;
    }
    .footer-nav {
      display: flex;
      justify-content: center;
      gap: 24px;
      flex-wrap: wrap;
      margin-bottom: 24px;
    }
    .footer-nav a {
      color: #9a8070;
      text-decoration: none;
      transition: color 0.2s;
    }
    .footer-nav a:hover { color: var(--gold); }
    .footer-name {
      font-family: 'Noto Serif JP', serif;
      font-size: 14px;
      color: #b0a090;
      margin-bottom: 6px;
      letter-spacing: 0.12em;
    }

    /* ===== RESPONSIVE ===== */
    @media (max-width: 768px) {
      nav { padding: 14px 20px; }
      .nav-links { display: none; }
      .nav-hamburger { display: block; }

      .hero { height: auto; padding: 80px 24px 64px; }
      .hero-title { font-size: 28px; }
      .hero-daruma { display: none; }

      .greeting { padding: 56px 24px; }
      .greeting-title { font-size: 17px; }

      .features { grid-template-columns: 1fr; }
      .feat-card { border-right: none; border-bottom: 1px solid var(--border); }
      .feat-card:last-child { border-bottom: none; }

      .products { padding: 56px 20px; }
      .product-grid { grid-template-columns: repeat(2, 1fr); }

      .news { padding: 56px 24px; }
      .calendar-section { padding: 56px 24px; }
      .calendar-wrap { grid-template-columns: 1fr; }

      .sns-bar { flex-direction: column; gap: 16px; }
      footer { padding: 40px 24px; }
      .footer-nav { gap: 16px; }
      .divider { padding: 0 24px; }
    }

    @media (max-width: 480px) {
      .product-grid { grid-template-columns: 1fr 1fr; }
      .hero-title { font-size: 24px; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="/" class="nav-logo">
    だるま工房 吉んと
    <span>DARUMA KŌBŌ KICHINTO</span>
  </a>
  <ul class="nav-links" id="navLinks">
    <li><a href="/">ホーム</a></li>
    <li><a href="https://dreamgate.shopselect.net/items/all" target="_blank" rel="noopener">オンラインストア</a></li>
    <li><a href="/shop/">吉んとについて</a></li>
    <li><a href="/category/news/">News</a></li>
    <li><a href="/contact/">お問い合わせ</a></li>
  </ul>
  <div class="nav-right">
    <div class="nav-sns">
      <a href="https://www.facebook.com/740665426094407" target="_blank" rel="noopener" aria-label="Facebook">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
      </a>
      <a href="https://www.instagram.com/kichinto78" target="_blank" rel="noopener" aria-label="Instagram">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
      </a>
    </div>
    <a href="https://dreamgate.shopselect.net/cart/add/dreamgate-shopselect-net" target="_blank" rel="noopener" class="nav-cart">カート</a>
    <button class="nav-hamburger" onclick="toggleMenu()" aria-label="メニュー">
      <svg width="22" height="22" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <line x1="3" y1="6" x2="21" y2="6"/>
        <line x1="3" y1="12" x2="21" y2="12"/>
        <line x1="3" y1="18" x2="21" y2="18"/>
      </svg>
    </button>
  </div>
</nav>

<!-- HERO -->
<section class="hero" style="height: auto; min-height: 480px; padding: 0; display: block; position: relative; overflow: hidden;">
  <img
    src="スクリーンショット_2026-06-28_17_03_00.png"
    alt="だるま工房 吉んと — 本物の群馬だるま"
    style="width: 100%; height: 100%; object-fit: cover; display: block; max-height: 560px;"
  >
  <div style="
    position: absolute;
    bottom: 0; left: 0; right: 0;
    padding: 32px 48px;
    background: linear-gradient(to top, rgba(20,10,3,0.72) 0%, transparent 100%);
    display: flex;
    align-items: flex-end;
    justify-content: flex-end;
  ">
    <a href="https://dreamgate.shopselect.net/items/all" target="_blank" rel="noopener" class="hero-cta">
      だるまを選ぶ →
    </a>
  </div>
</section>

<!-- GREETING -->
<section class="greeting">
  <p class="section-label">ごあいさつ</p>
  <h2 class="greeting-title">吉(良きこと)が うんと(たくさん) ありますように</h2>
  <p class="greeting-body">
    手にした人がご自身の願いや目標への想いをより強くできる。<br>
    だるまさんを手にし、願いを込めて片目を描き入れることで<br>
    「よし！これできっと叶う。」と心持を前向きにされることで<br>
    行動にも違いが表れ、よい結果がもたらされることでしょう。<br><br>
    それが縁起物としての達磨さんの役割だと考えています。
  </p>
</section>

<div class="divider" aria-hidden="true">
  <div class="divider-line"></div>
  <div class="divider-mark">✦ ✦ ✦</div>
  <div class="divider-line"></div>
</div>

<!-- FEATURES -->
<section class="features" aria-label="吉んとの特徴">
  <a href="/about/" class="feat-card">
    <svg class="feat-icon" viewBox="0 0 72 72" aria-hidden="true">
      <ellipse cx="36" cy="48" rx="26" ry="22" fill="#c0392b" opacity="0.12"/>
      <ellipse cx="36" cy="40" rx="20" ry="20" fill="#d44e3a" opacity="0.2"/>
      <text x="36" y="48" text-anchor="middle" font-size="30" fill="#c0392b" font-family="serif">達</text>
    </svg>
    <div class="feat-title">ここを吉んと</div>
    <p class="feat-desc">達磨大師の意志の強さにあやかる縁起物。細部まで力強さを込めた、職人の一点もの。</p>
  </a>
  <a href="/media/" class="feat-card">
    <svg class="feat-icon" viewBox="0 0 72 72" aria-hidden="true">
      <rect x="10" y="20" width="52" height="34" rx="4" fill="#e8a050" opacity="0.15"/>
      <rect x="14" y="24" width="44" height="26" rx="2" fill="#e8a050" opacity="0.2"/>
      <text x="36" y="42" text-anchor="middle" font-size="18" fill="#b5451e">TV</text>
      <circle cx="36" cy="58" r="3" fill="#e8a050" opacity="0.5"/>
    </svg>
    <div class="feat-title">メディア掲載情報</div>
    <p class="feat-desc">テレビや雑誌にも取り上げられた吉んとのだるまさん。各メディア掲載実績はこちら。</p>
  </a>
  <a href="/%e3%83%95%e3%82%a9%e3%83%88%e3%82%ae%e3%83%a3%e3%83%a9%e3%83%aa%e3%83%bc/" class="feat-card">
    <svg class="feat-icon" viewBox="0 0 72 72" aria-hidden="true">
      <rect x="8" y="18" width="56" height="40" rx="6" fill="#c8a050" opacity="0.12"/>
      <circle cx="36" cy="36" r="12" fill="#c8a050" opacity="0.2"/>
      <circle cx="36" cy="36" r="6" fill="#c8a050" opacity="0.4"/>
      <circle cx="52" cy="24" r="4" fill="#e8a050" opacity="0.3"/>
    </svg>
    <div class="feat-title">フォトギャラリー</div>
    <p class="feat-desc">工房の様子や完成作品を多数掲載。だるまさんの表情や細部の仕上げをご覧ください。</p>
  </a>
</section>

<!-- PRODUCTS -->
<section class="products">
  <div class="section-header">
    <p class="section-label">Online Store</p>
    <h2 class="section-title">お勧め商品</h2>
  </div>
  <div class="product-grid">

    <!-- 福だるま -->
    <a href="https://dreamgate.shopselect.net/items/all" target="_blank" rel="noopener" class="product-card">
      <div class="product-img">
        <svg width="80" height="96" viewBox="0 0 80 96" aria-label="福だるま">
          <ellipse cx="40" cy="62" rx="32" ry="30" fill="#c0392b"/>
          <ellipse cx="40" cy="50" rx="24" ry="24" fill="#d44e3a"/>
          <ellipse cx="40" cy="41" rx="17" ry="15" fill="#f5ede8"/>
          <ellipse cx="30" cy="39" rx="6" ry="6.5" fill="#1a1a1a"/>
          <ellipse cx="50" cy="39" rx="6" ry="6.5" fill="#fff" stroke="#ccc" stroke-width="0.4"/>
          <ellipse cx="50" cy="39" rx="2.5" ry="2.8" fill="#1a1a1a"/>
          <path d="M33 50 Q40 56 47 50" stroke="#8a3020" stroke-width="1.5" fill="none"/>
          <ellipse cx="40" cy="75" rx="28" ry="12" fill="#9b2d1f"/>
          <text x="40" y="90" text-anchor="middle" font-size="9" fill="#e8c880" font-family="serif" letter-spacing="2">福　だ　る　ま</text>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">福だるま</div>
        <div class="product-tag">定番の縁起もの</div>
      </div>
    </a>

    <!-- 名入れだるま -->
    <a href="https://dreamgate.shopselect.net/items/all" target="_blank" rel="noopener" class="product-card">
      <div class="product-img">
        <svg width="80" height="96" viewBox="0 0 80 96" aria-label="名入れだるま">
          <ellipse cx="40" cy="62" rx="32" ry="30" fill="#7b3f00"/>
          <ellipse cx="40" cy="50" rx="24" ry="24" fill="#9b5010"/>
          <ellipse cx="40" cy="41" rx="17" ry="15" fill="#f5ede8"/>
          <ellipse cx="30" cy="39" rx="6" ry="6.5" fill="#1a1a1a"/>
          <ellipse cx="50" cy="39" rx="6" ry="6.5" fill="#1a1a1a"/>
          <text x="40" y="30" text-anchor="middle" font-size="9" fill="#c8a050" font-family="serif">吉</text>
          <ellipse cx="40" cy="75" rx="28" ry="12" fill="#5a2d00"/>
          <text x="40" y="90" text-anchor="middle" font-size="9" fill="#e8c880" font-family="serif" letter-spacing="2">名入れだるま</text>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">名入れだるま</div>
        <div class="product-tag">オーダーメイド</div>
      </div>
    </a>

    <!-- 必勝だるま -->
    <a href="https://dreamgate.shopselect.net/items/all" target="_blank" rel="noopener" class="product-card">
      <div class="product-img">
        <svg width="80" height="96" viewBox="0 0 80 96" aria-label="必勝だるま">
          <ellipse cx="40" cy="62" rx="32" ry="30" fill="#1a3a8a"/>
          <ellipse cx="40" cy="50" rx="24" ry="24" fill="#2a4a9a"/>
          <ellipse cx="40" cy="41" rx="17" ry="15" fill="#f5ede8"/>
          <ellipse cx="30" cy="39" rx="6" ry="6.5" fill="#1a1a1a"/>
          <ellipse cx="50" cy="39" rx="6" ry="6.5" fill="#fff"/>
          <ellipse cx="50" cy="39" rx="2.5" ry="2.8" fill="#1a1a1a"/>
          <text x="40" y="55" text-anchor="middle" font-size="9" fill="#e8c050" font-family="serif">必勝</text>
          <ellipse cx="40" cy="75" rx="28" ry="12" fill="#0a2060"/>
          <text x="40" y="90" text-anchor="middle" font-size="9" fill="#e8c880" font-family="serif" letter-spacing="2">必勝だるま</text>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">必勝だるま</div>
        <div class="product-tag">勝負ごとに</div>
      </div>
    </a>

    <!-- 合格だるま -->
    <a href="https://dreamgate.shopselect.net/items/all" target="_blank" rel="noopener" class="product-card">
      <div class="product-img">
        <svg width="80" height="96" viewBox="0 0 80 96" aria-label="合格だるま">
          <ellipse cx="40" cy="62" rx="32" ry="30" fill="#c8820a"/>
          <ellipse cx="40" cy="50" rx="24" ry="24" fill="#e09a20"/>
          <ellipse cx="40" cy="41" rx="17" ry="15" fill="#f5ede8"/>
          <ellipse cx="30" cy="39" rx="6" ry="6.5" fill="#1a1a1a"/>
          <ellipse cx="50" cy="39" rx="6" ry="6.5" fill="#fff"/>
          <ellipse cx="50" cy="39" rx="2.5" ry="2.8" fill="#1a1a1a"/>
          <text x="40" y="55" text-anchor="middle" font-size="9" fill="#4a2a00" font-family="serif">合格</text>
          <ellipse cx="40" cy="75" rx="28" ry="12" fill="#8a5a00"/>
          <text x="40" y="90" text-anchor="middle" font-size="9" fill="#e8c880" font-family="serif" letter-spacing="2">合格だるま</text>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">合格だるま</div>
        <div class="product-tag">受験・試験に</div>
      </div>
    </a>

    <!-- オリジナルだるま -->
    <a href="https://dreamgate.shopselect.net/items/all" target="_blank" rel="noopener" class="product-card">
      <div class="product-img">
        <svg width="80" height="96" viewBox="0 0 80 96" aria-label="オリジナルだるま">
          <ellipse cx="40" cy="62" rx="32" ry="30" fill="#2d7a3a"/>
          <ellipse cx="40" cy="50" rx="24" ry="24" fill="#3d8a4a"/>
          <ellipse cx="40" cy="41" rx="17" ry="15" fill="#f5ede8"/>
          <ellipse cx="30" cy="39" rx="6" ry="6.5" fill="#1a1a1a"/>
          <ellipse cx="50" cy="39" rx="6" ry="6.5" fill="#fff"/>
          <ellipse cx="50" cy="39" rx="2.5" ry="2.8" fill="#1a1a1a"/>
          <text x="40" y="55" text-anchor="middle" font-size="7" fill="#e8f8e8" font-family="serif">オリジナル</text>
          <ellipse cx="40" cy="75" rx="28" ry="12" fill="#1a5028"/>
          <text x="40" y="90" text-anchor="middle" font-size="9" fill="#e8c880" font-family="serif" letter-spacing="1">オリジナル</text>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">オリジナルだるま</div>
        <div class="product-tag">世界でひとつ</div>
      </div>
    </a>

    <!-- 咲だるま -->
    <a href="https://dreamgate.shopselect.net/items/all" target="_blank" rel="noopener" class="product-card">
      <div class="product-img">
        <svg width="80" height="96" viewBox="0 0 80 96" aria-label="咲だるま">
          <ellipse cx="40" cy="62" rx="32" ry="30" fill="#7a2d8a"/>
          <ellipse cx="40" cy="50" rx="24" ry="24" fill="#9a3da0"/>
          <ellipse cx="40" cy="41" rx="17" ry="15" fill="#f5ede8"/>
          <ellipse cx="30" cy="39" rx="6" ry="6.5" fill="#1a1a1a"/>
          <ellipse cx="50" cy="39" rx="6" ry="6.5" fill="#fff"/>
          <ellipse cx="50" cy="39" rx="2.5" ry="2.8" fill="#1a1a1a"/>
          <text x="40" y="55" text-anchor="middle" font-size="9" fill="#f8d0f8" font-family="serif">咲</text>
          <ellipse cx="40" cy="75" rx="28" ry="12" fill="#501a60"/>
          <text x="40" y="90" text-anchor="middle" font-size="9" fill="#e8c880" font-family="serif" letter-spacing="2">咲　だ　る　ま</text>
        </svg>
      </div>
      <div class="product-info">
        <div class="product-name">咲だるま</div>
        <div class="product-tag">花咲くように</div>
      </div>
    </a>

  </div>
  <div style="text-align: center; margin-top: 48px;">
    <a href="https://dreamgate.shopselect.net/items/all" target="_blank" rel="noopener" style="
      display: inline-block;
      border: 1px solid var(--red);
      color: var(--red);
      text-decoration: none;
      padding: 14px 56px;
      font-size: 13px;
      letter-spacing: 0.2em;
      border-radius: 2px;
      transition: background 0.2s, color 0.2s;
    " onmouseover="this.style.background='#c0392b';this.style.color='#fff'" onmouseout="this.style.background='transparent';this.style.color='#c0392b'">
      オンラインショップで全商品を見る →
    </a>
  </div>
</section>

<!-- NEWS -->
<section class="news">
  <div class="section-header">
    <p class="section-label">News</p>
    <h2 class="section-title">お知らせ</h2>
  </div>
  <div class="news-list">
    <div class="news-item">
      <span class="news-date">2020.11.08</span>
      <a href="/2020/11/08/%e3%81%a0%e3%82%8b%e3%81%be%e5%b7%a5%e6%88%bf%e5%90%89%e3%82%93%e3%81%a8%e5%85%ac%e5%bc%8f%e3%82%b5%e3%82%a4%e3%83%88%e3%82%aa%e3%83%bc%e3%83%97%e3%83%b3/" class="news-link">
        だるま工房吉んと 公式サイトオープン
      </a>
    </div>
  </div>
  <a href="/category/news/" class="news-more">一覧を見る →</a>
</section>

<!-- CALENDAR -->
<section class="calendar-section">
  <div class="section-header">
    <p class="section-label">Business Calendar</p>
    <h2 class="section-title">営業日カレンダー</h2>
  </div>
  <div class="calendar-wrap" id="calendarWrap">
    <!-- JS で生成 -->
  </div>
  <div style="text-align:center; margin-top: 16px;" class="cal-legend" style="justify-content: center;">
    <div class="cal-legend-dot" style="background: #ddd;"></div>
    <span style="font-size: 11px; color: var(--brown-lt);">発送業務休日</span>
  </div>
</section>

<!-- SNS BAR -->
<div class="sns-bar">
  <span class="sns-label">Follow us</span>
  <a href="https://www.facebook.com/740665426094407" class="sns-link" target="_blank" rel="noopener">
    <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true"><path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/></svg>
    Facebook
  </a>
  <a href="https://www.instagram.com/kichinto78" class="sns-link" target="_blank" rel="noopener">
    <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" aria-hidden="true"><rect x="2" y="2" width="20" height="20" rx="5"/><path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
    @kichinto78
  </a>
</div>

<!-- FOOTER -->
<footer>
  <nav class="footer-nav" aria-label="フッターナビ">
    <a href="/">ホーム</a>
    <a href="/about/">ここを吉んと</a>
    <a href="/shop/">吉んとについて</a>
    <a href="/usces-cart/">カート</a>
    <a href="/pay/">お支払方法</a>
    <a href="/send/">送料</a>
    <a href="/check/">特定商取引法に基づく表記</a>
    <a href="/privacy-policy/">個人情報の保護方針</a>
    <a href="/contact/">お問い合わせ</a>
  </nav>
  <p class="footer-name">だるま工房 吉んと</p>
  <p>© 2020 Daruma Kōbō Kichinto. All rights reserved.</p>
</footer>

<script>
  // ===== ハンバーガーメニュー =====
  function toggleMenu() {
    const nav = document.getElementById('navLinks');
    if (nav.style.display === 'flex') {
      nav.style.display = 'none';
    } else {
      nav.style.cssText = 'display:flex; flex-direction:column; position:absolute; top:56px; left:0; right:0; background:#fff; padding:16px 24px; border-bottom:1px solid #e0d4c0; gap:14px; z-index:300;';
    }
  }

  // ===== カレンダー生成 =====
  (function buildCalendar() {
    const wrap = document.getElementById('calendarWrap');
    const now = new Date();
    const months = [
      { year: now.getFullYear(), month: now.getMonth() },
      { year: now.getMonth() === 11 ? now.getFullYear() + 1 : now.getFullYear(), month: (now.getMonth() + 1) % 12 }
    ];
    const labels = ['今月', '翌月'];
    const DOW = ['日','月','火','水','木','金','土'];
    const JP_MONTHS = ['1月','2月','3月','4月','5月','6月','7月','8月','9月','10月','11月','12月'];

    months.forEach(function(m, idx) {
      const block = document.createElement('div');
      block.className = 'cal-block';

      const title = document.createElement('h3');
      title.textContent = labels[idx] + '（' + m.year + '年 ' + JP_MONTHS[m.month] + '）';
      block.appendChild(title);

      const table = document.createElement('table');
      table.className = 'cal-table';
      const thead = document.createElement('thead');
      const headRow = document.createElement('tr');
      DOW.forEach(function(d, i) {
        const th = document.createElement('th');
        th.textContent = d;
        if (i === 0) th.className = 'sun';
        if (i === 6) th.className = 'sat';
        headRow.appendChild(th);
      });
      thead.appendChild(headRow);
      table.appendChild(thead);

      const tbody = document.createElement('tbody');
      const firstDay = new Date(m.year, m.month, 1).getDay();
      const daysInMonth = new Date(m.year, m.month + 1, 0).getDate();
      let day = 1;
      for (let row = 0; row < 6; row++) {
        const tr = document.createElement('tr');
        for (let col = 0; col < 7; col++) {
          const td = document.createElement('td');
          if (row === 0 && col < firstDay || day > daysInMonth) {
            td.textContent = '';
          } else {
            td.textContent = day;
            const isToday = idx === 0 && day === now.getDate();
            if (isToday) td.className = 'today';
            else if (col === 0) td.className = 'sun';
            else if (col === 6) td.className = 'sat';
            day++;
          }
          tr.appendChild(td);
        }
        tbody.appendChild(tr);
        if (day > daysInMonth) break;
      }
      table.appendChild(tbody);
      block.appendChild(table);
      wrap.appendChild(block);
    });
  })();
</script>
</body>
</html>
