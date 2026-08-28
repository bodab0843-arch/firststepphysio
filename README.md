[index.html.html](https://github.com/user-attachments/files/31553025/index.html.html)
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta http-equiv="Content-Security-Policy" content="default-src 'self' 'unsafe-inline' 'unsafe-eval' https: data: blob:;">
<title>First Step | علاج طبيعي منزلي</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Reem+Kufi:wght@400;500;600;700&family=Tajawal:wght@300;400;500;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #F1F4EE;
    --bg-card: #FBF8F1;
    --ink: #16302E;
    --teal: #2F6F63;
    --teal-deep: #1D4A41;
    --ochre: #D68A3C;
    --ochre-deep: #B96F27;
    --cream: #F3E3C4;
    --line: #D8DED3;
  }
  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    background: var(--bg);
    color: var(--ink);
    font-family: 'Tajawal', sans-serif;
    line-height: 1.7;
    overflow-x: hidden;
  }
  h1,h2,h3, .kufi{ font-family: 'Reem Kufi', sans-serif; }
  a{ color: inherit; text-decoration: none; }
  img,svg{ display:block; }
  .wrap{
    max-width: 1080px;
    margin: 0 auto;
    padding: 0 24px;
  }
  .visually-hidden{
    position:absolute; width:1px;height:1px;overflow:hidden;clip:rect(0 0 0 0);
  }

  /* ---------- HEADER ---------- */
  header{
    position: sticky; top:0; z-index: 50;
    background: rgba(241,244,238,0.9);
    backdrop-filter: blur(8px);
    border-bottom: 1px solid var(--line);
  }
  .nav{
    display:flex; align-items:center; justify-content: space-between;
    padding: 14px 24px;
    max-width: 1080px; margin:0 auto;
  }
  .logo{
    display:flex; align-items:center; gap:10px;
    font-family:'Reem Kufi', sans-serif;
    font-size: 1.35rem;
    color: var(--teal-deep);
  }
  .logo .dot{ color: var(--ochre); }
  .nav-actions{ display:flex; align-items:center; gap:14px; }
  .call-link{
    display:flex; align-items:center; gap:6px;
    font-size:.92rem; font-weight:700; color: var(--teal-deep);
    white-space:nowrap;
  }
  .btn{
    display:inline-flex; align-items:center; justify-content:center; gap:8px;
    padding: 12px 22px;
    border-radius: 999px;
    font-weight:700;
    font-size: .95rem;
    border: none;
    cursor:pointer;
    transition: transform .15s ease, box-shadow .15s ease;
  }
  .btn:focus-visible{ outline: 3px solid var(--ochre-deep); outline-offset: 3px; }
  .btn:hover{ transform: translateY(-2px); }
  .btn-primary{
    background: var(--ochre);
    color: #fff;
    box-shadow: 0 8px 20px -8px rgba(214,138,60,.6);
  }
  .btn-primary:hover{ background: var(--ochre-deep); }
  .btn-ghost{
    background: transparent;
    border: 1.5px solid var(--teal);
    color: var(--teal-deep);
    padding: 10px 20px;
  }
  .nav .btn{ padding: 10px 18px; font-size: .88rem; }

  /* ---------- HERO ---------- */
  .hero{
    padding: 72px 0 40px;
    position: relative;
  }
  .hero-grid{
    display:grid;
    grid-template-columns: 1.1fr .9fr;
    gap: 48px;
    align-items:center;
  }
  .eyebrow{
    display:inline-flex; align-items:center; gap:8px;
    font-size: .82rem; font-weight:700; letter-spacing:.02em;
    color: var(--teal-deep);
    background: var(--cream);
    padding: 6px 14px;
    border-radius: 999px;
    margin-bottom: 18px;
  }
  .eyebrow::before{
    content:''; width:7px; height:7px; border-radius:50%;
    background: var(--ochre);
  }
  .hero h1{
    font-size: clamp(2.1rem, 4.4vw, 3.2rem);
    color: var(--teal-deep);
    line-height: 1.25;
    margin-bottom: 20px;
  }
  .hero h1 span{ color: var(--ochre); }
  .hero p{
    font-size: 1.08rem;
    color: #3c534f;
    max-width: 46ch;
    margin-bottom: 30px;
  }
  .hero-actions{ display:flex; gap:14px; flex-wrap:wrap; }

  /* signature: recovery path illustration */
  .hero-art{
    position: relative;
    aspect-ratio: 1/1;
    display:flex; align-items:center; justify-content:center;
  }
  .hero-art svg{ width: 100%; height:100%; }
  .path-dash{
    stroke-dasharray: 6 10;
    animation: dashmove 3.5s linear infinite;
  }
  @keyframes dashmove{ to{ stroke-dashoffset: -160; } }
  .step-pulse{ animation: pulse 2.4s ease-in-out infinite; transform-origin: center; }
  @keyframes pulse{ 0%,100%{ transform: scale(1);} 50%{ transform: scale(1.14);} }

  /* ---------- FOOTSTEP DIVIDER (signature element) ---------- */
  .steps-divider{
    max-width: 1080px; margin: 8px auto 0;
    padding: 30px 24px 10px;
    display:flex; align-items:flex-end; justify-content:space-between;
    position: relative;
  }
  .steps-divider::before{
    content:'';
    position:absolute; right:24px; left:24px; top:52%;
    border-top: 2px dashed var(--line);
    z-index:0;
  }
  .footprint{
    width: 16px; height: 26px;
    color: var(--teal);
    opacity:.75;
    position:relative; z-index:1;
    background: var(--bg);
  }
  .footprint:nth-child(even){ transform: translateY(14px) rotate(-8deg); }
  .footprint:nth-child(odd){ transform: translateY(-4px) rotate(8deg); }
  .footprint svg{ width:100%; height:100%; }

  /* ---------- SECTION SHARED ---------- */
  section{ padding: 56px 0; }
  .section-head{ max-width: 620px; margin-bottom: 40px; }
  .section-head .eyebrow{ margin-bottom: 14px; }
  .section-head h2{
    font-size: clamp(1.6rem, 3vw, 2.2rem);
    color: var(--teal-deep);
    margin-bottom: 10px;
  }
  .section-head p{ color: #3c534f; }

  /* ---------- WHO IT'S FOR ---------- */
  .cards{
    display:grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 20px;
  }
  .card{
    background: var(--bg-card);
    border: 1px solid var(--line);
    border-radius: 18px;
    padding: 26px 20px;
    transition: box-shadow .2s ease, transform .2s ease;
  }
  .card:hover{ box-shadow: 0 14px 30px -18px rgba(29,74,65,.35); transform: translateY(-3px); }
  .card .icon{
    width: 42px; height:42px;
    color: var(--teal-deep);
    margin-bottom: 16px;
  }
  .card h3{ font-size: 1.08rem; margin-bottom: 8px; color: var(--teal-deep); }
  .card p{ font-size: .92rem; color: #52655f; }

  /* ---------- HOW IT WORKS ---------- */
  .how-grid{
    display:grid; grid-template-columns: repeat(3, 1fr); gap: 28px;
  }
  .how-item{ position:relative; padding-top: 6px; }
  .how-num{
    font-family:'Reem Kufi', sans-serif;
    font-size: 2.6rem;
    color: var(--cream);
    -webkit-text-stroke: 1.5px var(--ochre-deep);
    line-height:1;
    margin-bottom: 14px;
    display:block;
  }
  .how-item h3{ font-size: 1.1rem; margin-bottom: 8px; color: var(--teal-deep); }
  .how-item p{ color: #52655f; font-size: .95rem; }

  /* ---------- BOOKING FORM ---------- */
  .booking{
    background: var(--teal-deep);
    border-radius: 28px;
    color: #EFF4EF;
    padding: 48px;
    position: relative;
    overflow:hidden;
  }
  .booking::after{
    content:'';
    position:absolute; inset:0;
    background: radial-gradient(circle at 90% 10%, rgba(214,138,60,.18), transparent 55%);
    pointer-events:none;
  }
  .booking-grid{
    display:grid; grid-template-columns: .9fr 1.1fr; gap: 44px;
    position:relative; z-index:1;
  }
  .booking-intro .eyebrow{ background: rgba(243,227,196,.15); color: #F3E3C4; }
  .booking-intro h2{ color:#fff; font-size: clamp(1.5rem,2.6vw,2rem); margin-bottom: 14px; }
  .booking-intro p{ color: #C9D8D2; margin-bottom: 20px; }
  .trust-line{
    display:flex; gap: 10px; align-items:center;
    font-size: .88rem; color:#C9D8D2; margin-bottom:10px;
  }
  .trust-line svg{ width:18px; height:18px; color: var(--ochre); flex-shrink:0; }

  form{ display:flex; flex-direction:column; gap:16px; }
  .field label{
    display:block; font-size: .86rem; font-weight:700; margin-bottom: 6px; color:#EFF4EF;
  }
  .field input, .field textarea{
    width:100%;
    padding: 13px 16px;
    border-radius: 12px;
    border: 1.5px solid rgba(255,255,255,.18);
    background: rgba(255,255,255,.06);
    color:#fff;
    font-family:'Tajawal', sans-serif;
    font-size: .95rem;
  }
  .field input::placeholder, .field textarea::placeholder{ color: rgba(239,244,239,.45); }
  .field input:focus, .field textarea:focus{
    outline: none; border-color: var(--ochre);
    background: rgba(255,255,255,.09);
  }
  .row-2{ display:grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .form-actions{ display:flex; align-items:center; gap:16px; flex-wrap:wrap; margin-top: 6px; }
  .link-email{ font-size: .88rem; font-weight:700; color:#F3E3C4; border-bottom: 1px dashed #F3E3C4; }
  .form-note{ font-size: .78rem; color:#9FB4AD; margin-top: 6px; }
  #formStatus{ font-size:.88rem; font-weight:700; min-height: 20px; }
  #formStatus.ok{ color:#BFE6A8; }
  #formStatus.err{ color:#F2B6A6; }

  /* ---------- FOOTER ---------- */
  footer{
    padding: 40px 0 28px;
    border-top: 1px solid var(--line);
    margin-top: 30px;
  }
  .footer-grid{
    display:flex; justify-content:space-between; align-items:flex-start; flex-wrap:wrap; gap: 20px;
  }
  .footer-grid .logo{ margin-bottom: 8px; }
  .footer-grid p{ color:#52655f; font-size:.9rem; max-width: 40ch; }
  .footer-contact{ font-size:.92rem; }
  .footer-contact div{ margin-bottom: 6px; color: var(--teal-deep); font-weight:700; }

  /* ---------- WHATSAPP FAB ---------- */
  .wa-fab{
    position: fixed; bottom: 22px; left: 22px; z-index: 60;
    width: 58px; height:58px; border-radius:50%;
    background: var(--teal);
    display:flex; align-items:center; justify-content:center;
    box-shadow: 0 10px 26px -8px rgba(29,74,65,.55);
    color:#fff;
  }
  .wa-fab:hover{ background: var(--teal-deep); }
  .wa-fab svg{ width: 28px; height:28px; }

  /* ---------- RESPONSIVE ---------- */
  @media (max-width: 860px){
    .hero-grid{ grid-template-columns: 1fr; }
    .hero-art{ max-width: 280px; margin: 0 auto; order:-1; }
    .cards{ grid-template-columns: repeat(2,1fr); }
    .how-grid{ grid-template-columns: 1fr; gap: 30px; }
    .booking{ padding: 30px 22px; }
    .booking-grid{ grid-template-columns: 1fr; gap: 28px; }
    .row-2{ grid-template-columns: 1fr; }
    .footer-grid{ flex-direction:column; }
    .call-link span.long{ display:none; }
  }
  @media (max-width:520px){
    .cards{ grid-template-columns: 1fr; }
    .footprint:nth-child(n+6){ display:none; }
  }

  @media (prefers-reduced-motion: reduce){
    .path-dash, .step-pulse{ animation: none; }
  }
</style>
</head>
<body>

<header>
  <nav class="nav">
    <div class="logo">First <span class="dot">Step</span></div>
    <div class="nav-actions">
      <a class="call-link" href="tel:+201025783234">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72c.127.96.361 1.903.7 2.81a2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
        <span class="long">01025783234</span>
      </a>
      <a class="btn btn-primary" href="#booking">احجز دلوقتي</a>
    </div>
  </nav>
</header>

<main>
  <!-- HERO -->
  <section class="hero">
    <div class="wrap hero-grid">
      <div>
        <span class="eyebrow">علاج طبيعي في بيتك</span>
        <h1>أول خطوة للرجوع تتحرك<br><span>من غير ما تسيب البيت</span></h1>
        <p>معالج طبيعي متخصص ييجيلك في بيتك بجدول يناسبك، من غير عناء المواصلات أو الانتظار في العيادة. إحنا معاك من أول خطوة لحد الرجوع تتحرك بثقة.</p>
        <div class="hero-actions">
          <a class="btn btn-primary" href="#booking">احجز جلسة الآن</a>
          <a class="btn btn-ghost" href="#how">إزاي بتحصل؟</a>
        </div>
      </div>
      <div class="hero-art" aria-hidden="true">
        <svg viewBox="0 0 300 300" fill="none">
          <path class="path-dash" d="M40 230 Q90 260 130 200 T220 150 T260 70" stroke="#2F6F63" stroke-width="4" stroke-linecap="round"/>
          <circle class="step-pulse" cx="40" cy="230" r="9" fill="#D68A3C"/>
          <circle cx="130" cy="200" r="6" fill="#2F6F63"/>
          <circle cx="220" cy="150" r="6" fill="#2F6F63"/>
          <circle class="step-pulse" cx="260" cy="70" r="9" fill="#D68A3C" style="animation-delay:1.2s"/>
        </svg>
      </div>
    </div>
  </section>

  <!-- footstep divider -->
  <div class="steps-divider" aria-hidden="true">
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
  </div>

  <!-- WHO IT'S FOR -->
  <section id="who">
    <div class="wrap">
      <div class="section-head">
        <span class="eyebrow">لمين الخدمة</span>
        <h2>مصممة لكل حالة محتاجة رعاية في بيتها</h2>
        <p>لو التنقل بقى صعب أو متعب، إحنا بنيجيلك بدل ما تيجي إحنا.</p>
      </div>
      <div class="cards">
        <div class="card">
          <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="5" r="2.2"/><path d="M9 22l1-8-2-2 1-6 3-1 3 1 1 6-2 2 1 8"/><path d="M6 22h5M13 22h5"/></svg></div>
          <h3>كبار السن</h3>
          <p>متابعة حركة وتوازن وتقوية عضلات بأمان جوه البيت.</p>
        </div>
        <div class="card">
          <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><rect x="4" y="9" width="16" height="7" rx="2"/><path d="M9 9V7a3 3 0 0 1 6 0v2"/><path d="M12 12h.01"/></svg></div>
          <h3>ما بعد العمليات</h3>
          <p>برنامج تأهيل تدريجي بعد الجراحة يرجعك لحياتك بسرعة وأمان.</p>
        </div>
        <div class="card">
          <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M13 4l-3 7h4l-3 9 8-11h-4l3-5z"/></svg></div>
          <h3>إصابات رياضية</h3>
          <p>علاج وتقوية للعودة للملعب أو النشاط اليومي من غير ما تتكرر الإصابة.</p>
        </div>
        <div class="card">
          <div class="icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round" stroke-linejoin="round"><path d="M12 3v18M8 7c0 2 4 2 4 4s-4 2-4 4M16 7c0 2-4 2-4 4s4 2 4 4"/></svg></div>
          <h3>آلام الظهر والمفاصل</h3>
          <p>جلسات مخصصة لتخفيف الألم المزمن وتحسين المرونة والحركة.</p>
        </div>
      </div>
    </div>
  </section>

  <div class="steps-divider" aria-hidden="true">
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
    <div class="footprint"><svg viewBox="0 0 24 40"><path d="M12 2C8.5 2 6.5 5.5 6.5 10c0 2.6.9 4.3 1.4 6.8.4 2.2-.4 3.7-1.6 6-1.4 2.6-2.3 5.2-2.3 8.2 0 4.4 3.5 7 8 7s8-2.6 8-7c0-3-.9-5.6-2.3-8.2-1.2-2.3-2-3.8-1.6-6 .5-2.5 1.4-4.2 1.4-6.8 0-4.5-2-8-8-8z" fill="currentColor"/></svg></div>
  </div>

  <!-- HOW IT WORKS -->
  <section id="how">
    <div class="wrap">
      <div class="section-head">
        <span class="eyebrow">إزاي بتحصل</span>
        <h2>من الحجز لحد أول جلسة… ٣ خطوات بس</h2>
      </div>
      <div class="how-grid">
        <div class="how-item">
          <span class="how-num">١</span>
          <h3>تحجز بياناتك</h3>
          <p>تملى الاسم والسن والعنوان ورقم التواصل، وتبعتها لنا في ثواني.</p>
        </div>
        <div class="how-item">
          <span class="how-num">٢</span>
          <h3>نتصل نأكد الميعاد</h3>
          <p>فريقنا يكلمك يحدد أنسب معاد ويسألك عن حالتك بالتفصيل.</p>
        </div>
        <div class="how-item">
          <span class="how-num">٣</span>
          <h3>المعالج ييجي بيتك</h3>
          <p>يوصلك في الميعاد بكل الأدوات، ويبدأ برنامج العلاج المناسب لحالتك.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- BOOKING -->
  <section id="booking">
    <div class="wrap">
      <div class="booking">
        <div class="booking-grid">
          <div class="booking-intro">
            <span class="eyebrow">احجز جلستك</span>
            <h2>خطوتك الأولى نحو الحركة تبدأ هنا</h2>
            <p>املأ البيانات وهتتبعت لينا على طول، وهنتواصل معاك لتأكيد الميعاد.</p>
            <div class="trust-line">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M9 12l2 2 4-4"/><circle cx="12" cy="12" r="9"/></svg>
              بياناتك بتوصل لينا مباشرة، من غير أي طرف تالت
            </div>
            <div class="trust-line">
              <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 8v4l3 3"/><circle cx="12" cy="12" r="9"/></svg>
              هنتصل بيك خلال ساعات لتأكيد أقرب ميعاد
            </div>
          </div>

          <form id="bookingForm" novalidate>
            <div class="field">
              <label for="name">الاسم بالكامل</label>
              <input type="text" id="name" name="name" placeholder="مثال: أحمد محمود" required>
            </div>
            <div class="row-2">
              <div class="field">
                <label for="age">السن</label>
                <input type="number" id="age" name="age" min="1" max="120" placeholder="مثال: 65" required>
              </div>
              <div class="field">
                <label for="phone">رقم التواصل</label>
                <input type="tel" id="phone" name="phone" placeholder="01xxxxxxxxx" required>
              </div>
            </div>
            <div class="field">
              <label for="address">العنوان بالتفصيل</label>
              <textarea id="address" name="address" rows="3" placeholder="المحافظة، المنطقة، الشارع، رقم العمارة والدور" required></textarea>
            </div>
            <div class="form-actions">
              <button type="submit" class="btn btn-primary">
                <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M17.5 14.4c-.3-.1-1.7-.9-2-1-.3-.1-.5-.1-.7.1-.2.3-.8 1-.9 1.2-.2.2-.3.2-.6.1-.3-.1-1.3-.5-2.4-1.5-.9-.8-1.5-1.8-1.7-2.1-.2-.3 0-.5.1-.6.1-.1.3-.3.4-.5.1-.1.2-.3.3-.5.1-.2 0-.4 0-.5-.1-.1-.7-1.6-.9-2.2-.2-.6-.5-.5-.7-.5h-.6c-.2 0-.5.1-.8.4-.3.3-1 1-1 2.4s1 2.8 1.2 3c.1.2 2 3 4.8 4.3.7.3 1.2.5 1.6.6.7.2 1.3.2 1.8.1.5-.1 1.7-.7 1.9-1.3.2-.6.2-1.2.2-1.3-.1-.1-.3-.2-.6-.3z"/><path d="M12 2a10 10 0 0 0-8.5 15.2L2 22l4.9-1.5A10 10 0 1 0 12 2z" fill="none" stroke="currentColor" stroke-width="1.2"/></svg>
                ابعت الحجز على واتساب
              </button>
              <a href="#" id="emailLink" class="link-email">أو ابعته بالإيميل بدل كده</a>
            </div>
            <p id="formStatus" role="status"></p>
            <p class="form-note">هيتفتحلك واتساب أو الإيميل ببياناتك جاهزة عشان تبعتها بضغطة واحدة.</p>
          </form>
        </div>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap footer-grid">
    <div>
      <div class="logo">First <span class="dot">Step</span></div>
      <p>خدمة علاج طبيعي منزلي بتوصلك في بيتك بكل الأدوات والخبرة اللازمة لرجوعك تتحرك براحتك.</p>
    </div>
    <div class="footer-contact">
      <div>واتساب / تليفون: 01025783234</div>
      <div>الإيميل: algamdidahoom@gmail.com</div>
    </div>
  </div>
</footer>

<a class="wa-fab" href="https://wa.me/201025783234?text=%D8%B9%D8%A7%D9%8A%D8%B2%20%D8%A7%D8%B3%D8%AA%D9%81%D8%B3%D8%B1%20%D8%B9%D9%86%20%D8%AC%D9%84%D8%B3%D8%A7%D8%AA%20%D8%A7%D9%84%D8%B9%D9%84%D8%A7%D8%AC%20%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%D8%B9%D9%8A%20%D8%A7%D9%84%D9%85%D9%86%D8%B2%D9%84%D9%8A" target="_blank" rel="noopener" aria-label="تواصل عبر واتساب">
  <svg viewBox="0 0 24 24" fill="currentColor"><path d="M17.5 14.4c-.3-.1-1.7-.9-2-1-.3-.1-.5-.1-.7.1-.2.3-.8 1-.9 1.2-.2.2-.3.2-.6.1-.3-.1-1.3-.5-2.4-1.5-.9-.8-1.5-1.8-1.7-2.1-.2-.3 0-.5.1-.6.1-.1.3-.3.4-.5.1-.1.2-.3.3-.5.1-.2 0-.4 0-.5-.1-.1-.7-1.6-.9-2.2-.2-.6-.5-.5-.7-.5h-.6c-.2 0-.5.1-.8.4-.3.3-1 1-1 2.4s1 2.8 1.2 3c.1.2 2 3 4.8 4.3.7.3 1.2.5 1.6.6.7.2 1.3.2 1.8.1.5-.1 1.7-.7 1.9-1.3.2-.6.2-1.2.2-1.3-.1-.1-.3-.2-.6-.3z"/><path d="M12 2a10 10 0 0 0-8.5 15.2L2 22l4.9-1.5A10 10 0 1 0 12 2z" fill="none" stroke="currentColor" stroke-width="1.4"/></svg>
</a>

<script>
  const WHATSAPP_NUMBER = "201025783234";
  const EMAIL = "algamdidahoom@gmail.com";
  const form = document.getElementById('bookingForm');
  const status = document.getElementById('formStatus');
  const emailLink = document.getElementById('emailLink');

  function buildMessage(){
    const name = document.getElementById('name').value.trim();
    const age = document.getElementById('age').value.trim();
    const phone = document.getElementById('phone').value.trim();
    const address = document.getElementById('address').value.trim();
    return {
      name, age, phone, address,
      text: `طلب حجز جلسة علاج طبيعي منزلي - First Step\nالاسم: ${name}\nالسن: ${age}\nالعنوان: ${address}\nرقم التواصل: ${phone}`
    };
  }

  function validate(name, age, phone, address){
    if(!name || !age || !phone || !address){
      return "من فضلك املأ كل الحقول قبل الإرسال.";
    }
    if(!/^0?1[0-9]{9,10}$/.test(phone.replace(/\s|-/g,''))){
      return "من فضلك تأكد من رقم التليفون.";
    }
    return null;
  }

  form.addEventListener('submit', function(e){
    e.preventDefault();
    const {name, age, phone, address, text} = buildMessage();
    const error = validate(name, age, phone, address);
    if(error){
      status.textContent = error;
      status.className = 'err';
      return;
    }
    const url = `https://wa.me/${WHATSAPP_NUMBER}?text=${encodeURIComponent(text)}`;
    window.open(url, '_blank');
    status.textContent = "تم فتح واتساب ببياناتك، اضغط إرسال هناك لتأكيد الحجز.";
    status.className = 'ok';
  });

  emailLink.addEventListener('click', function(e){
    e.preventDefault();
    const {name, age, phone, address, text} = buildMessage();
    const error = validate(name, age, phone, address);
    if(error){
      status.textContent = error;
      status.className = 'err';
      return;
    }
    const subject = encodeURIComponent("طلب حجز جلسة علاج طبيعي منزلي - First Step");
    const body = encodeURIComponent(text);
    window.location.href = `mailto:${EMAIL}?subject=${subject}&body=${body}`;
    status.textContent = "تم فتح برنامج الإيميل ببياناتك، دوس إرسال لتأكيد الحجز.";
    status.className = 'ok';
  });
</script>

</body>
</html>
