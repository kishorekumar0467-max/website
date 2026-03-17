<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Surya & Co – Your Trusted Mobile Destination in Hosur</title>
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --bg: #0a0a0f;
      --surface: #12121a;
      --card: #1a1a28;
      --accent: #ff5f1f;
      --accent2: #ffb347;
      --gold: #f7c948;
      --text: #f0eeea;
      --muted: #888899;
      --border: rgba(255,255,255,0.07);
      --glow: rgba(255,95,31,0.25);
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      font-family: 'DM Sans', sans-serif;
      background: var(--bg);
      color: var(--text);
      overflow-x: hidden;
    }

    /* ── NAV ── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      display: flex; align-items: center; justify-content: space-between;
      padding: 18px 5%;
      background: rgba(10,10,15,0.85);
      backdrop-filter: blur(14px);
      border-bottom: 1px solid var(--border);
    }
    .nav-logo {
      font-family: 'Syne', sans-serif;
      font-weight: 800; font-size: 1.35rem;
      color: var(--text);
      letter-spacing: -0.5px;
    }
    .nav-logo span { color: var(--accent); }
    .nav-links { display: flex; gap: 32px; list-style: none; }
    .nav-links a {
      color: var(--muted); text-decoration: none;
      font-size: 0.9rem; font-weight: 500;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--text); }
    .nav-cta {
      background: var(--accent);
      color: #fff; padding: 10px 22px;
      border-radius: 8px; text-decoration: none;
      font-size: 0.88rem; font-weight: 600;
      transition: background 0.2s, transform 0.15s;
    }
    .nav-cta:hover { background: #e04e10; transform: translateY(-1px); }

    /* ── HERO ── */
    #home {
      min-height: 100vh;
      display: flex; flex-direction: column;
      align-items: center; justify-content: center;
      text-align: center;
      padding: 100px 5% 60px;
      position: relative;
      overflow: hidden;
    }
    .hero-bg {
      position: absolute; inset: 0;
      background:
        radial-gradient(ellipse 70% 55% at 50% 20%, rgba(255,95,31,0.18) 0%, transparent 60%),
        radial-gradient(ellipse 50% 40% at 80% 80%, rgba(247,201,72,0.08) 0%, transparent 60%);
      pointer-events: none;
    }
    .hero-badge {
      display: inline-flex; align-items: center; gap: 8px;
      background: rgba(255,95,31,0.12); border: 1px solid rgba(255,95,31,0.3);
      color: var(--accent2); padding: 6px 16px; border-radius: 99px;
      font-size: 0.8rem; font-weight: 600; letter-spacing: 0.8px;
      text-transform: uppercase; margin-bottom: 28px;
      animation: fadeUp 0.7s ease both;
    }
    .hero-title {
      font-family: 'Syne', sans-serif;
      font-size: clamp(3rem, 8vw, 6.5rem);
      font-weight: 800; line-height: 1.0;
      letter-spacing: -2px;
      margin-bottom: 16px;
      animation: fadeUp 0.7s 0.1s ease both;
    }
    .hero-title .amp { color: var(--accent); }
    .hero-title .co { color: var(--gold); }
    .hero-sub {
      font-size: clamp(1rem, 2.5vw, 1.25rem);
      color: var(--muted); max-width: 520px;
      line-height: 1.6; margin-bottom: 44px;
      font-style: italic;
      animation: fadeUp 0.7s 0.2s ease both;
    }
    .hero-actions {
      display: flex; gap: 14px; flex-wrap: wrap; justify-content: center;
      animation: fadeUp 0.7s 0.3s ease both;
    }
    .btn-primary {
      display: inline-flex; align-items: center; gap: 8px;
      background: var(--accent); color: #fff;
      padding: 14px 32px; border-radius: 10px;
      font-size: 1rem; font-weight: 600; text-decoration: none;
      transition: background 0.2s, transform 0.15s, box-shadow 0.2s;
      box-shadow: 0 0 0 0 var(--glow);
    }
    .btn-primary:hover {
      background: #e04e10; transform: translateY(-2px);
      box-shadow: 0 8px 32px var(--glow);
    }
    .btn-outline {
      display: inline-flex; align-items: center; gap: 8px;
      border: 1.5px solid rgba(255,255,255,0.2);
      color: var(--text); padding: 14px 32px;
      border-radius: 10px; font-size: 1rem; font-weight: 500;
      text-decoration: none; transition: border-color 0.2s, background 0.2s;
    }
    .btn-outline:hover { border-color: var(--accent); background: rgba(255,95,31,0.07); }
    .hero-stats {
      display: flex; gap: 40px; margin-top: 64px; flex-wrap: wrap; justify-content: center;
      animation: fadeUp 0.7s 0.4s ease both;
    }
    .stat { text-align: center; }
    .stat-num {
      font-family: 'Syne', sans-serif;
      font-size: 2rem; font-weight: 800; color: var(--accent);
    }
    .stat-label { font-size: 0.8rem; color: var(--muted); margin-top: 2px; }

    /* ── SECTION COMMON ── */
    section { padding: 90px 5%; }
    .section-label {
      font-size: 0.75rem; letter-spacing: 2.5px; text-transform: uppercase;
      color: var(--accent); font-weight: 700; margin-bottom: 12px;
    }
    .section-title {
      font-family: 'Syne', sans-serif;
      font-size: clamp(2rem, 4vw, 3rem);
      font-weight: 800; line-height: 1.1;
      letter-spacing: -1px; margin-bottom: 14px;
    }
    .section-sub {
      color: var(--muted); font-size: 1rem;
      max-width: 500px; line-height: 1.6; margin-bottom: 48px;
    }

    /* ── PRODUCTS ── */
    #products { background: var(--surface); }
    .products-header { text-align: center; }
    .products-header .section-sub { margin-left: auto; margin-right: auto; }
    .products-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 22px;
    }
    .product-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px; overflow: hidden;
      transition: transform 0.22s, box-shadow 0.22s, border-color 0.22s;
    }
    .product-card:hover {
      transform: translateY(-6px);
      box-shadow: 0 20px 50px rgba(0,0,0,0.4);
      border-color: rgba(255,95,31,0.3);
    }
    .product-img {
      width: 100%; height: 200px;
      display: flex; align-items: center; justify-content: center;
      background: linear-gradient(135deg, #1e1e2e 0%, #2a2a3e 100%);
      font-size: 5rem;
      position: relative; overflow: hidden;
    }
    .product-img::after {
      content: '';
      position: absolute; inset: 0;
      background: radial-gradient(circle at 50% 60%, rgba(255,95,31,0.1), transparent 70%);
    }
    .product-badge {
      position: absolute; top: 12px; right: 12px;
      background: var(--accent); color: #fff;
      font-size: 0.7rem; font-weight: 700;
      padding: 4px 10px; border-radius: 99px;
      letter-spacing: 0.5px;
    }
    .product-body { padding: 20px; }
    .product-brand { font-size: 0.72rem; color: var(--accent); font-weight: 700; letter-spacing: 1px; text-transform: uppercase; margin-bottom: 4px; }
    .product-name { font-family: 'Syne', sans-serif; font-size: 1.1rem; font-weight: 700; margin-bottom: 10px; }
    .product-specs { list-style: none; margin-bottom: 16px; }
    .product-specs li {
      font-size: 0.8rem; color: var(--muted);
      padding: 4px 0; border-bottom: 1px solid var(--border);
      display: flex; justify-content: space-between;
    }
    .product-specs li span { color: var(--text); font-weight: 500; }
    .product-footer { display: flex; align-items: center; justify-content: space-between; margin-top: 16px; }
    .product-price { font-family: 'Syne', sans-serif; font-size: 1.3rem; font-weight: 800; color: var(--gold); }
    .product-price small { font-size: 0.7rem; color: var(--muted); font-family: 'DM Sans'; font-weight: 400; display: block; }
    .enquire-btn {
      background: transparent; border: 1.5px solid var(--accent);
      color: var(--accent); padding: 8px 18px; border-radius: 8px;
      font-size: 0.82rem; font-weight: 600; cursor: pointer;
      transition: background 0.18s, color 0.18s;
    }
    .enquire-btn:hover { background: var(--accent); color: #fff; }

    /* ── CALL BANNER ── */
    .call-banner {
      background: linear-gradient(135deg, #ff5f1f 0%, #ff8c42 100%);
      padding: 50px 5%;
      display: flex; align-items: center; justify-content: space-between;
      flex-wrap: wrap; gap: 24px;
    }
    .call-banner-text h2 {
      font-family: 'Syne', sans-serif;
      font-size: clamp(1.6rem, 3vw, 2.4rem);
      font-weight: 800; color: #fff; margin-bottom: 6px;
    }
    .call-banner-text p { color: rgba(255,255,255,0.8); font-size: 1rem; }
    .call-now-btn {
      display: inline-flex; align-items: center; gap: 10px;
      background: #fff; color: var(--accent);
      padding: 16px 36px; border-radius: 12px;
      font-size: 1.1rem; font-weight: 700; text-decoration: none;
      font-family: 'Syne', sans-serif;
      box-shadow: 0 8px 30px rgba(0,0,0,0.2);
      transition: transform 0.15s, box-shadow 0.15s;
      white-space: nowrap;
    }
    .call-now-btn:hover { transform: scale(1.04); box-shadow: 0 12px 40px rgba(0,0,0,0.3); }
    .call-icon { font-size: 1.3rem; animation: ring 1.5s ease infinite; }
    @keyframes ring {
      0%,100%{transform:rotate(0)} 20%{transform:rotate(-15deg)} 40%{transform:rotate(15deg)} 60%{transform:rotate(-10deg)} 80%{transform:rotate(10deg)}
    }

    /* ── FEEDBACK ── */
    #feedback {
      background: var(--bg);
      display: grid; grid-template-columns: 1fr 1fr; gap: 64px; align-items: start;
    }
    @media(max-width: 800px) { #feedback { grid-template-columns: 1fr; } }
    .feedback-info { padding-top: 8px; }
    .info-item {
      display: flex; align-items: flex-start; gap: 16px;
      margin-bottom: 28px;
    }
    .info-icon {
      width: 44px; height: 44px; border-radius: 12px;
      background: rgba(255,95,31,0.12); border: 1px solid rgba(255,95,31,0.2);
      display: flex; align-items: center; justify-content: center;
      font-size: 1.2rem; flex-shrink: 0;
    }
    .info-text strong { display: block; font-weight: 600; margin-bottom: 2px; }
    .info-text span { color: var(--muted); font-size: 0.9rem; }
    .form-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 20px; padding: 36px;
    }
    .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
    @media(max-width: 500px) { .form-row { grid-template-columns: 1fr; } }
    .form-group { margin-bottom: 18px; }
    .form-group label { display: block; font-size: 0.82rem; font-weight: 600; color: var(--muted); margin-bottom: 7px; letter-spacing: 0.5px; }
    .form-group input,
    .form-group select,
    .form-group textarea {
      width: 100%;
      background: var(--surface);
      border: 1.5px solid var(--border);
      color: var(--text);
      padding: 12px 16px; border-radius: 10px;
      font-size: 0.93rem; font-family: 'DM Sans', sans-serif;
      outline: none;
      transition: border-color 0.2s;
    }
    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus { border-color: var(--accent); }
    .form-group textarea { resize: vertical; min-height: 90px; }
    .form-group select option { background: #1a1a28; }
    .submit-btn {
      width: 100%; background: var(--accent); color: #fff;
      border: none; padding: 15px; border-radius: 10px;
      font-size: 1rem; font-weight: 700; cursor: pointer;
      font-family: 'Syne', sans-serif;
      transition: background 0.2s, transform 0.15s;
    }
    .submit-btn:hover { background: #e04e10; transform: translateY(-2px); }
    .success-msg {
      display: none; background: rgba(0,200,100,0.1);
      border: 1px solid rgba(0,200,100,0.3);
      color: #4dff9b; padding: 14px 18px; border-radius: 10px;
      font-size: 0.9rem; font-weight: 500; margin-top: 16px; text-align: center;
    }

    /* ── CONTACT ── */
    #contact { background: var(--surface); }
    .contact-grid {
      display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 20px;
    }
    .contact-card {
      background: var(--card); border: 1px solid var(--border);
      border-radius: 16px; padding: 28px 24px; text-align: center;
      transition: border-color 0.2s, transform 0.2s;
    }
    .contact-card:hover { border-color: rgba(255,95,31,0.3); transform: translateY(-4px); }
    .contact-card-icon { font-size: 2.2rem; margin-bottom: 14px; }
    .contact-card h3 { font-family: 'Syne', sans-serif; font-size: 1rem; font-weight: 700; margin-bottom: 6px; }
    .contact-card p { color: var(--muted); font-size: 0.88rem; line-height: 1.5; }
    .contact-card a { color: var(--accent); text-decoration: none; }
    .contact-card a:hover { text-decoration: underline; }

    /* ── FOOTER ── */
    footer {
      background: var(--bg); border-top: 1px solid var(--border);
      padding: 48px 5% 28px;
    }
    .footer-inner {
      display: flex; justify-content: space-between; flex-wrap: wrap; gap: 36px;
      margin-bottom: 36px;
    }
    .footer-brand { max-width: 260px; }
    .footer-logo {
      font-family: 'Syne', sans-serif; font-weight: 800; font-size: 1.3rem;
      margin-bottom: 12px;
    }
    .footer-logo span { color: var(--accent); }
    .footer-desc { color: var(--muted); font-size: 0.88rem; line-height: 1.6; }
    .footer-links h4 { font-family: 'Syne', sans-serif; font-weight: 700; margin-bottom: 14px; font-size: 0.9rem; }
    .footer-links ul { list-style: none; }
    .footer-links li { margin-bottom: 9px; }
    .footer-links a { color: var(--muted); text-decoration: none; font-size: 0.88rem; transition: color 0.18s; }
    .footer-links a:hover { color: var(--accent); }
    .social-icons { display: flex; gap: 12px; margin-top: 16px; }
    .social-btn {
      width: 38px; height: 38px; border-radius: 10px;
      background: var(--card); border: 1px solid var(--border);
      display: flex; align-items: center; justify-content: center;
      font-size: 1rem; text-decoration: none;
      transition: border-color 0.18s, background 0.18s;
    }
    .social-btn:hover { border-color: var(--accent); background: rgba(255,95,31,0.1); }
    .footer-bottom {
      border-top: 1px solid var(--border);
      padding-top: 20px; text-align: center;
      color: var(--muted); font-size: 0.8rem;
    }
    .footer-bottom span { color: var(--accent); }

    /* ── ANIMATIONS ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(28px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    .fade-in {
      opacity: 0; transform: translateY(24px);
      transition: opacity 0.55s ease, transform 0.55s ease;
    }
    .fade-in.visible { opacity: 1; transform: none; }

    /* ── MOBILE NAV ── */
    @media(max-width: 700px) {
      .nav-links { display: none; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Surya <span>&</span> Co</div>
  <ul class="nav-links">
    <li><a href="#home">Home</a></li>
    <li><a href="#products">Products</a></li>
    <li><a href="#feedback">Enquiry</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a href="tel:9361104622" class="nav-cta">📞 Call Now</a>
</nav>

<!-- HERO -->
<section id="home">
  <div class="hero-bg"></div>
  <div class="hero-badge">📍 Based in Hosur, Tamil Nadu</div>
  <h1 class="hero-title">Surya <span class="amp">&</span> <span class="co">Co</span></h1>
  <p class="hero-sub">Your Trusted Mobile Destination in Hosur — premium phones, genuine prices, expert advice.</p>
  <div class="hero-actions">
    <a href="#products" class="btn-primary">📱 Browse Mobiles</a>
    <a href="#feedback" class="btn-outline">✉️ Send Enquiry</a>
  </div>
  <div class="hero-stats">
    <div class="stat"><div class="stat-num">500+</div><div class="stat-label">Happy Customers</div></div>
    <div class="stat"><div class="stat-num">50+</div><div class="stat-label">Mobile Models</div></div>
    <div class="stat"><div class="stat-num">5★</div><div class="stat-label">Rated Service</div></div>
    <div class="stat"><div class="stat-num">3+</div><div class="stat-label">Years in Business</div></div>
  </div>
</section>

<!-- PRODUCTS -->
<section id="products">
  <div class="products-header fade-in">
    <div class="section-label">Our Collection</div>
    <h2 class="section-title">Featured Mobiles</h2>
    <p class="section-sub">Explore our handpicked range of the latest smartphones — all at the best prices in Hosur.</p>
  </div>
  <div class="products-grid">

    <div class="product-card fade-in">
      <div class="product-img">📱<div class="product-badge">New</div></div>
      <div class="product-body">
        <div class="product-brand">Samsung</div>
        <div class="product-name">Galaxy S24 FE</div>
        <ul class="product-specs">
          <li>Display <span>6.7" AMOLED</span></li>
          <li>Camera <span>50 MP Triple</span></li>
          <li>Battery <span>4700 mAh</span></li>
          <li>RAM / Storage <span>8GB / 128GB</span></li>
        </ul>
        <div class="product-footer">
          <div class="product-price">₹42,999<small>Best Price Guaranteed</small></div>
          <button class="enquire-btn" onclick="scrollToForm('Samsung Galaxy S24 FE')">Enquire</button>
        </div>
      </div>
    </div>

    <div class="product-card fade-in">
      <div class="product-img">📱<div class="product-badge">Hot</div></div>
      <div class="product-body">
        <div class="product-brand">Apple</div>
        <div class="product-name">iPhone 15</div>
        <ul class="product-specs">
          <li>Display <span>6.1" Super Retina</span></li>
          <li>Camera <span>48 MP Dual</span></li>
          <li>Battery <span>3877 mAh</span></li>
          <li>RAM / Storage <span>6GB / 128GB</span></li>
        </ul>
        <div class="product-footer">
          <div class="product-price">₹69,999<small>Best Price Guaranteed</small></div>
          <button class="enquire-btn" onclick="scrollToForm('Apple iPhone 15')">Enquire</button>
        </div>
      </div>
    </div>

    <div class="product-card fade-in">
      <div class="product-img">📱<div class="product-badge">Value</div></div>
      <div class="product-body">
        <div class="product-brand">Redmi</div>
        <div class="product-name">Note 13 Pro</div>
        <ul class="product-specs">
          <li>Display <span>6.67" AMOLED</span></li>
          <li>Camera <span>200 MP Triple</span></li>
          <li>Battery <span>5100 mAh</span></li>
          <li>RAM / Storage <span>8GB / 256GB</span></li>
        </ul>
        <div class="product-footer">
          <div class="product-price">₹24,999<small>Best Price Guaranteed</small></div>
          <button class="enquire-btn" onclick="scrollToForm('Redmi Note 13 Pro')">Enquire</button>
        </div>
      </div>
    </div>

    <div class="product-card fade-in">
      <div class="product-img">📱<div class="product-badge">Popular</div></div>
      <div class="product-body">
        <div class="product-brand">OnePlus</div>
        <div class="product-name">Nord CE 4</div>
        <ul class="product-specs">
          <li>Display <span>6.7" AMOLED 120Hz</span></li>
          <li>Camera <span>50 MP Dual</span></li>
          <li>Battery <span>5500 mAh</span></li>
          <li>RAM / Storage <span>8GB / 128GB</span></li>
        </ul>
        <div class="product-footer">
          <div class="product-price">₹24,999<small>Best Price Guaranteed</small></div>
          <button class="enquire-btn" onclick="scrollToForm('OnePlus Nord CE 4')">Enquire</button>
        </div>
      </div>
    </div>

    <div class="product-card fade-in">
      <div class="product-img">📱<div class="product-badge">New</div></div>
      <div class="product-body">
        <div class="product-brand">Vivo</div>
        <div class="product-name">V40 Pro</div>
        <ul class="product-specs">
          <li>Display <span>6.78" AMOLED</span></li>
          <li>Camera <span>50 MP Zeiss Triple</span></li>
          <li>Battery <span>5500 mAh</span></li>
          <li>RAM / Storage <span>12GB / 256GB</span></li>
        </ul>
        <div class="product-footer">
          <div class="product-price">₹49,999<small>Best Price Guaranteed</small></div>
          <button class="enquire-btn" onclick="scrollToForm('Vivo V40 Pro')">Enquire</button>
        </div>
      </div>
    </div>

    <div class="product-card fade-in">
      <div class="product-img">📱<div class="product-badge">Budget</div></div>
      <div class="product-body">
        <div class="product-brand">Realme</div>
        <div class="product-name">C65 5G</div>
        <ul class="product-specs">
          <li>Display <span>6.67" LCD 90Hz</span></li>
          <li>Camera <span>50 MP Dual</span></li>
          <li>Battery <span>5000 mAh</span></li>
          <li>RAM / Storage <span>6GB / 128GB</span></li>
        </ul>
        <div class="product-footer">
          <div class="product-price">₹12,999<small>Best Price Guaranteed</small></div>
          <button class="enquire-btn" onclick="scrollToForm('Realme C65 5G')">Enquire</button>
        </div>
      </div>
    </div>

  </div>
</section>

<!-- CALL BANNER -->
<div class="call-banner fade-in">
  <div class="call-banner-text">
    <h2>Can't find what you're looking for?</h2>
    <p>Call us directly — we'll help you find the perfect phone at the right price.</p>
  </div>
  <a href="tel:9361104622" class="call-now-btn">
    <span class="call-icon">📞</span> Call Now: 93611 04622
  </a>
</div>

<!-- FEEDBACK / ENQUIRY -->
<section id="feedback">
  <div class="feedback-info fade-in">
    <div class="section-label">Get In Touch</div>
    <h2 class="section-title">Send Us an Enquiry</h2>
    <p class="section-sub">Interested in a model? Fill in the form and we'll get back to you quickly.</p>

    <div class="info-item">
      <div class="info-icon">📍</div>
      <div class="info-text">
        <strong>Our Location</strong>
        <span>Hosur, Tamil Nadu</span>
      </div>
    </div>
    <div class="info-item">
      <div class="info-icon">📞</div>
      <div class="info-text">
        <strong>Phone Number</strong>
        <span><a href="tel:9361104622" style="color:var(--accent);text-decoration:none;">93611 04622</a></span>
      </div>
    </div>
    <div class="info-item">
      <div class="info-icon">✉️</div>
      <div class="info-text">
        <strong>Email Address</strong>
        <span><a href="mailto:kishorekumar0467@gmail.com" style="color:var(--accent);text-decoration:none;">kishorekumar0467@gmail.com</a></span>
      </div>
    </div>
    <div class="info-item">
      <div class="info-icon">🕐</div>
      <div class="info-text">
        <strong>Working Hours</strong>
        <span>Mon – Sat: 9:00 AM – 8:00 PM</span>
      </div>
    </div>
  </div>

  <div class="form-card fade-in">
    <h3 style="font-family:'Syne',sans-serif;font-weight:700;margin-bottom:24px;font-size:1.3rem;">Enquiry Form</h3>
    <div class="form-row">
      <div class="form-group">
        <label>Your Name *</label>
        <input type="text" id="fname" placeholder="Full name" />
      </div>
      <div class="form-group">
        <label>Phone Number *</label>
        <input type="tel" id="fphone" placeholder="10-digit number" />
      </div>
    </div>
    <div class="form-group">
      <label>Email Address</label>
      <input type="email" id="femail" placeholder="your@email.com" />
    </div>
    <div class="form-group">
      <label>Mobile Model Interested In *</label>
      <select id="fmodel">
        <option value="">— Select a model —</option>
        <option>Samsung Galaxy S24 FE</option>
        <option>Apple iPhone 15</option>
        <option>Redmi Note 13 Pro</option>
        <option>OnePlus Nord CE 4</option>
        <option>Vivo V40 Pro</option>
        <option>Realme C65 5G</option>
        <option>Other (mention below)</option>
      </select>
    </div>
    <div class="form-group">
      <label>Message / Requirements</label>
      <textarea id="fmsg" placeholder="Any specific requirements, budget, colour preferences..."></textarea>
    </div>
    <button class="submit-btn" onclick="submitForm()">Submit Enquiry →</button>
    <div class="success-msg" id="successMsg">
      ✅ Thank you! We'll contact you within 24 hours.
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div style="text-align:center" class="fade-in">
    <div class="section-label">Find Us</div>
    <h2 class="section-title">Contact Surya & Co</h2>
    <p class="section-sub" style="margin:0 auto 48px;">We're always here to help you choose the right mobile.</p>
  </div>
  <div class="contact-grid fade-in">
    <div class="contact-card">
      <div class="contact-card-icon">📍</div>
      <h3>Address</h3>
      <p>Hosur, Tamil Nadu, India</p>
    </div>
    <div class="contact-card">
      <div class="contact-card-icon">📞</div>
      <h3>Phone</h3>
      <p><a href="tel:9361104622">93611 04622</a></p>
    </div>
    <div class="contact-card">
      <div class="contact-card-icon">✉️</div>
      <h3>Email</h3>
      <p><a href="mailto:kishorekumar0467@gmail.com">kishorekumar0467@gmail.com</a></p>
    </div>
    <div class="contact-card">
      <div class="contact-card-icon">🕐</div>
      <h3>Working Hours</h3>
      <p>Mon – Sat<br>9:00 AM – 8:00 PM</p>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div class="footer-brand">
      <div class="footer-logo">Surya <span>&</span> Co</div>
      <p class="footer-desc">Your Trusted Mobile Destination in Hosur. Genuine phones, best prices, and expert guidance — always.</p>
      <div class="social-icons">
        <a href="#" class="social-btn" title="Facebook">📘</a>
        <a href="#" class="social-btn" title="Instagram">📷</a>
        <a href="#" class="social-btn" title="WhatsApp">💬</a>
      </div>
    </div>
    <div class="footer-links">
      <h4>Quick Links</h4>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#products">Products</a></li>
        <li><a href="#feedback">Enquiry</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>
    <div class="footer-links">
      <h4>Popular Brands</h4>
      <ul>
        <li><a href="#products">Samsung</a></li>
        <li><a href="#products">Apple iPhone</a></li>
        <li><a href="#products">Redmi / Xiaomi</a></li>
        <li><a href="#products">OnePlus</a></li>
        <li><a href="#products">Vivo & Realme</a></li>
      </ul>
    </div>
    <div class="footer-links">
      <h4>Contact</h4>
      <ul>
        <li><a href="tel:9361104622">📞 93611 04622</a></li>
        <li><a href="mailto:kishorekumar0467@gmail.com">✉️ Email Us</a></li>
        <li><a href="#contact">📍 Hosur, Tamil Nadu</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    © 2025 <span>Surya & Co</span>. All rights reserved. | Hosur's Trusted Mobile Shop
  </div>
</footer>

<script>
  // Scroll animations
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.12 });
  document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

  // Pre-fill model in form from product cards
  function scrollToForm(model) {
    document.getElementById('fmodel').value = model;
    document.getElementById('feedback').scrollIntoView({ behavior: 'smooth' });
  }

  // Form submit handler
  function submitForm() {
    const name = document.getElementById('fname').value.trim();
    const phone = document.getElementById('fphone').value.trim();
    const model = document.getElementById('fmodel').value;
    if (!name || !phone || !model) {
      alert('Please fill in your name, phone number, and the mobile model.');
      return;
    }
    document.getElementById('successMsg').style.display = 'block';
    document.getElementById('fname').value = '';
    document.getElementById('fphone').value = '';
    document.getElementById('femail').value = '';
    document.getElementById('fmodel').value = '';
    document.getElementById('fmsg').value = '';
    setTimeout(() => { document.getElementById('successMsg').style.display = 'none'; }, 5000);
  }
</script>
</body>
</html>
