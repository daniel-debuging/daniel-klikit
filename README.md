[klikit_inquiry.html](https://github.com/user-attachments/files/27901963/klikit_inquiry.html)
# daniel-klikit
Inquiry Form
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Integration Inquiry — Klikit Solutions</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,400&family=DM+Serif+Display&display=swap" rel="stylesheet" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/tabler-icons.min.css" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --bg: #0d0f1a;
    --surface: #151826;
    --surface2: #1c1f30;
    --border: rgba(255,255,255,0.08);
    --text: #f0f2f5;
    --muted: #8a8fa8;
    --hint: #555a72;
    --accent: #4ade80;
    --chip-active-bg: rgba(74,222,128,0.12);
    --radius: 10px;
    --radius-lg: 14px;
  }
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Sans', sans-serif;
    min-height: 100vh;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    padding: 2rem 1rem 4rem;
  }
  .page { width: 100%; max-width: 560px; animation: fadeUp 0.4s ease both; }
  @keyframes fadeUp { from { opacity:0; transform:translateY(16px); } to { opacity:1; transform:translateY(0); } }

  .logo { display: flex; align-items: center; gap: 10px; margin-bottom: 1.5rem; }
  .logo-box { width:40px; height:40px; background:linear-gradient(135deg,#22c55e,#4ade80); border-radius:10px; display:flex; align-items:center; justify-content:center; }
  .logo-box i { font-size:20px; color:#0d0f1a; }
  .logo-text { font-size:17px; font-weight:600; letter-spacing:-0.3px; }
  .logo-sub { font-size:11px; color:var(--muted); margin-top:1px; }

  .hero-eyebrow { font-size:12px; font-weight:500; color:var(--accent); letter-spacing:0.6px; text-transform:uppercase; margin-bottom:14px; }
  .hero-title { font-family:'DM Serif Display',serif; font-size:clamp(30px,6vw,42px); line-height:1.1; letter-spacing:-0.5px; margin-bottom:14px; }
  .hero-title span { color:var(--accent); font-style:italic; }
  .hero-sub { font-size:17px; font-weight:500; color:var(--text); margin-bottom:10px; letter-spacing:-0.2px; }
  .hero-desc { font-size:14px; color:var(--muted); line-height:1.7; margin-bottom:2.5rem; }

  .divider { border:none; border-top:1px solid var(--border); margin:1.75rem 0; }

  .section-label { font-size:11px; font-weight:500; color:var(--hint); letter-spacing:0.8px; text-transform:uppercase; margin-bottom:14px; display:flex; align-items:center; gap:8px; }
  .section-label::after { content:''; flex:1; height:1px; background:var(--border); }

  .field { margin-bottom:12px; }
  .field label { font-size:12px; color:var(--muted); display:block; margin-bottom:5px; font-weight:500; }
  .field input, .field textarea {
    width:100%; background:var(--surface); border:1px solid var(--border);
    border-radius:var(--radius); padding:11px 14px; font-size:14px;
    font-family:inherit; color:var(--text); outline:none;
    transition:border-color 0.15s, box-shadow 0.15s;
  }
  .field input::placeholder, .field textarea::placeholder { color:var(--hint); }
  .field input:focus, .field textarea:focus { border-color:var(--accent); box-shadow:0 0 0 3px rgba(74,222,128,0.1); }
  .field textarea { resize:vertical; line-height:1.6; min-height:80px; }
  .field.error input, .field.error textarea { border-color:#f87171; }
  .err-msg { font-size:11px; color:#f87171; margin-top:4px; min-height:16px; }
  .row { display:grid; grid-template-columns:1fr 1fr; gap:10px; }

  .chips { display:flex; flex-wrap:wrap; gap:8px; }
  .chip { display:flex; align-items:center; gap:7px; padding:8px 14px; border:1px solid var(--border); border-radius:20px; font-size:13px; cursor:pointer; color:var(--muted); background:var(--surface); transition:all 0.15s; user-select:none; }
  .chip i { font-size:15px; }
  .chip:hover { border-color:rgba(74,222,128,0.3); color:var(--text); }
  .chip.active { background:var(--chip-active-bg); border-color:var(--accent); color:var(--accent); }

  .outlet-row { display:grid; grid-template-columns:repeat(4,1fr); gap:8px; }
  .outlet-btn { padding:10px 0; background:var(--surface); border:1px solid var(--border); border-radius:var(--radius); font-size:14px; font-family:inherit; color:var(--muted); cursor:pointer; transition:all 0.15s; }
  .outlet-btn:hover { border-color:rgba(74,222,128,0.3); color:var(--text); }
  .outlet-btn.active { background:var(--chip-active-bg); border-color:var(--accent); color:var(--accent); font-weight:500; }

  .service-card { background:var(--surface); border:1px solid var(--border); border-radius:var(--radius-lg); padding:1rem 1.1rem; cursor:pointer; transition:all 0.15s; display:flex; align-items:flex-start; gap:13px; margin-bottom:10px; }
  .service-card:hover { border-color:rgba(74,222,128,0.3); }
  .service-card.active { border-color:var(--accent); background:rgba(74,222,128,0.06); }
  .svc-icon { width:38px; height:38px; flex-shrink:0; background:var(--surface2); border-radius:9px; display:flex; align-items:center; justify-content:center; }
  .svc-icon i { font-size:18px; color:var(--muted); }
  .service-card.active .svc-icon { background:rgba(74,222,128,0.15); }
  .service-card.active .svc-icon i { color:var(--accent); }
  .svc-body { flex:1; }
  .svc-title { font-size:14px; font-weight:500; color:var(--text); margin-bottom:3px; }
  .svc-desc { font-size:12px; color:var(--muted); line-height:1.6; }
  .svc-check { font-size:18px; color:var(--accent); opacity:0; transition:opacity 0.15s; margin-left:auto; flex-shrink:0; padding-top:2px; }
  .service-card.active .svc-check { opacity:1; }

  .submit-btn { width:100%; padding:14px; background:var(--accent); color:#0d0f1a; border:none; border-radius:var(--radius); font-size:15px; font-weight:600; font-family:inherit; cursor:pointer; display:flex; align-items:center; justify-content:center; gap:8px; transition:all 0.15s; margin-top:1.75rem; letter-spacing:-0.2px; }
  .submit-btn:hover { background:#22c55e; transform:translateY(-1px); }
  .submit-btn:active { transform:scale(0.98); }
  .submit-btn i { font-size:18px; }

  .footer-note { font-size:12px; color:var(--hint); text-align:center; margin-top:14px; line-height:1.7; }

  .success-view { text-align:center; padding:3rem 1rem; display:none; }
  .success-icon { width:70px; height:70px; background:rgba(74,222,128,0.12); border:1px solid var(--accent); border-radius:50%; display:flex; align-items:center; justify-content:center; margin:0 auto 1.25rem; }
  .success-icon i { font-size:32px; color:var(--accent); }
  .success-title { font-family:'DM Serif Display',serif; font-size:26px; margin-bottom:10px; }
  .success-desc { font-size:14px; color:var(--muted); line-height:1.8; margin-bottom:1.75rem; }
  .reset-btn { display:inline-flex; align-items:center; gap:7px; padding:10px 22px; background:var(--surface); border:1px solid var(--border); border-radius:var(--radius); color:var(--text); font-size:14px; font-family:inherit; cursor:pointer; transition:all 0.15s; }
  .reset-btn:hover { border-color:var(--accent); color:var(--accent); }

  @media (max-width:480px) {
    .row { grid-template-columns:1fr; }
    .outlet-row { grid-template-columns:repeat(2,1fr); }
  }
</style>
</head>
<body>
<div class="page">

  <div class="logo">
    <div class="logo-box"><i class="ti ti-devices"></i></div>
    <div>
      <div class="logo-text">Integration Solutions</div>
      <div class="logo-sub">Powered by Klikit</div>
    </div>
  </div>
  <p class="hero-eyebrow">Curious about multiplying your online deliveries?</p>
  <h1 class="hero-title"><span>1</span> Location.&nbsp; <span>3</span> Brands.<br/><span>9</span> Online Stores.</h1>
  <p class="hero-sub">One screen. All your deliveries. Let's talk.</p>
  <p class="hero-desc">Fill in your details below and we will reach out via WhatsApp to show you how it works.</p>

  <div id="formView">

    <div class="section-label">Contact info</div>
    <div class="row">
      <div class="field" id="f-name">
        <label>Your name</label>
        <input type="text" id="fname" placeholder="e.g. Ahmad" />
        <div class="err-msg" id="e-name"></div>
      </div>
      <div class="field" id="f-biz">
        <label>Business / brand name</label>
        <input type="text" id="biz" placeholder="e.g. Nasi Lemak Panas" />
        <div class="err-msg" id="e-biz"></div>
      </div>
    </div>
    <div class="row">
      <div class="field" id="f-phone">
        <label>WhatsApp number</label>
        <input type="tel" id="phone" placeholder="+60 12-XXX XXXX" />
        <div class="err-msg" id="e-phone"></div>
      </div>
      <div class="field">
        <label>Email <span style="color:var(--hint)">(optional)</span></label>
        <input type="email" id="email" placeholder="you@example.com" />
      </div>
    </div>

    <div class="divider"></div>

    <div class="section-label">Delivery platforms</div>
    <div style="font-size:13px; color:var(--muted); margin-bottom:10px;">Which platforms are you currently active on?</div>
    <div class="chips" id="platformChips" style="margin-bottom:1.5rem;">
      <div class="chip" data-val="GrabFood" onclick="toggleChip(this)"><i class="ti ti-motorcycle"></i> GrabFood</div>
      <div class="chip" data-val="FoodPanda" onclick="toggleChip(this)"><i class="ti ti-shopping-bag"></i> FoodPanda</div>
      <div class="chip" data-val="Shopee Food" onclick="toggleChip(this)"><i class="ti ti-brand-shopee"></i> Shopee Food</div>
      <div class="chip" data-val="Other" onclick="toggleChip(this)"><i class="ti ti-dots-circle-horizontal"></i> Other</div>
    </div>

    <div style="font-size:13px; color:var(--muted); margin-bottom:10px;">How many outlets do you have?</div>
    <div class="outlet-row" id="outletBtns" style="margin-bottom:1.5rem;">
      <button class="outlet-btn" data-val="1 outlet" onclick="selectOutlet(this)">1</button>
      <button class="outlet-btn" data-val="2-5 outlets" onclick="selectOutlet(this)">2 - 5</button>
      <button class="outlet-btn" data-val="6-10 outlets" onclick="selectOutlet(this)">6 - 10</button>
      <button class="outlet-btn" data-val="10+ outlets" onclick="selectOutlet(this)">10+</button>
    </div>

    <div class="divider"></div>

    <div class="section-label">What you need</div>
    <div style="font-size:13px; color:var(--muted); margin-bottom:12px;">Select all that apply.</div>

    <div class="service-card" data-val="Klikit Integration (device consolidation)" onclick="toggleService(this)">
      <div class="svc-icon"><i class="ti ti-plug-connected"></i></div>
      <div class="svc-body">
        <div class="svc-title">Klikit integration — reduce devices</div>
        <div class="svc-desc">Manage GrabFood, FoodPanda and Shopee Food orders from a single screen. No more tablet chaos.</div>
      </div>
      <i class="ti ti-circle-check svc-check"></i>
    </div>

    <div class="service-card" data-val="Menu Restructuring and Sales Consulting" onclick="toggleService(this)">
      <div class="svc-icon"><i class="ti ti-receipt"></i></div>
      <div class="svc-body">
        <div class="svc-title">Menu restructuring and sales consulting</div>
        <div class="svc-desc">Our partner helps optimise your online menu, costing, combos and pricing to grow delivery sales.</div>
      </div>
      <i class="ti ti-circle-check svc-check"></i>
    </div>

    <div class="service-card" data-val="Full Package (Integration + Consulting)" onclick="toggleService(this)">
      <div class="svc-icon"><i class="ti ti-sparkles"></i></div>
      <div class="svc-body">
        <div class="svc-title">Full package — integration and consulting</div>
        <div class="svc-desc">The complete solution: hardware consolidation plus a full delivery growth strategy.</div>
      </div>
      <i class="ti ti-circle-check svc-check"></i>
    </div>

    <div class="field" style="margin-top:1rem;">
      <label>Biggest pain point right now <span style="color:var(--hint)">(optional)</span></label>
      <textarea id="pain" placeholder="e.g. too many tablets to manage, missing orders, low rating on Grab, not sure how to price my menu..."></textarea>
    </div>

    <button class="submit-btn" onclick="submitForm()">
      <i class="ti ti-brand-whatsapp"></i> Send inquiry via WhatsApp
    </button>
    <p class="footer-note">
      Tapping the button will open WhatsApp with your details pre-filled.<br/>
      We will reply within 1 business day. No spam, no pressure.
    </p>

  </div>

  <div class="success-view" id="successView">
    <div class="success-icon"><i class="ti ti-check"></i></div>
    <div class="success-title">You are all set!</div>
    <p class="success-desc">
      Thanks <strong id="sName"></strong> — WhatsApp is opening with your inquiry details.<br/>
      We will get back to <strong id="sBiz"></strong> within 1 business day.
    </p>
    <button class="reset-btn" onclick="resetForm()"><i class="ti ti-refresh"></i> Submit another inquiry</button>
  </div>

</div>
<script>
  var WA = '601154543934';
  function toggleChip(el) { el.classList.toggle('active'); }
  function selectOutlet(el) {
    document.querySelectorAll('.outlet-btn').forEach(function(b){ b.classList.remove('active'); });
    el.classList.add('active');
  }
  function toggleService(el) { el.classList.toggle('active'); }
  function validate() {
    var ok = true;
    var checks = [
      {id:'fname', fid:'f-name', eid:'e-name', msg:'Please enter your name.'},
      {id:'biz',   fid:'f-biz',  eid:'e-biz',  msg:'Please enter your business name.'},
      {id:'phone', fid:'f-phone',eid:'e-phone', msg:'Please enter your WhatsApp number.'}
    ];
    checks.forEach(function(c){
      var v = document.getElementById(c.id).value.trim();
      var fe = document.getElementById(c.fid);
      var ee = document.getElementById(c.eid);
      if (!v) { fe.classList.add('error'); ee.textContent = c.msg; ok = false; }
      else { fe.classList.remove('error'); ee.textContent = ''; }
    });
    return ok;
  }
  function submitForm() {
    if (!validate()) return;
    var name  = document.getElementById('fname').value.trim();
    var biz   = document.getElementById('biz').value.trim();
    var phone = document.getElementById('phone').value.trim();
    var email = document.getElementById('email').value.trim();
    var pain  = document.getElementById('pain').value.trim();
    var platforms = [];
    document.querySelectorAll('#platformChips .chip.active').forEach(function(c){ platforms.push(c.dataset.val); });
    var ob = document.querySelector('.outlet-btn.active');
    var outlet = ob ? ob.dataset.val : 'Not specified';
    var services = [];
    document.querySelectorAll('.service-card.active').forEach(function(c){ services.push(c.dataset.val); });

    var lines = [
      '*New Client Inquiry*',
      '',
      'Name: ' + name,
      'Business: ' + biz,
      'WhatsApp: ' + phone
    ];
    if (email) lines.push('Email: ' + email);
    lines.push('');
    lines.push('Platforms: ' + (platforms.length ? platforms.join(', ') : 'Not selected'));
    lines.push('Outlets: ' + outlet);
    lines.push('Interested in: ' + (services.length ? services.join(', ') : 'Not selected'));
    if (pain) { lines.push(''); lines.push('Pain point: ' + pain); }
    lines.push('');
    lines.push('Sent via Klikit Inquiry Form');

    var url = 'https://wa.me/' + WA + '?text=' + encodeURIComponent(lines.join('\n'));
    document.getElementById('sName').textContent = name;
    document.getElementById('sBiz').textContent  = biz;
    document.getElementById('formView').style.display    = 'none';
    document.getElementById('successView').style.display = 'block';
    window.open(url, '_blank');
  }
  function resetForm() {
    document.getElementById('formView').style.display    = 'block';
    document.getElementById('successView').style.display = 'none';
    ['fname','biz','phone','email','pain'].forEach(function(id){ document.getElementById(id).value = ''; });
    document.querySelectorAll('.chip.active,.outlet-btn.active,.service-card.active').forEach(function(el){ el.classList.remove('active'); });
  }
</script>
</body>
</html>
