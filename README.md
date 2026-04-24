<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Rohan — Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@200;300;400;500&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{background:#f5f5f7;color:#1d1d1f;font-family:'Inter',system-ui,sans-serif;-webkit-font-smoothing:antialiased}
.wrap{max-width:760px;margin:0 auto;padding:2rem 1.5rem 3rem}

.hero{text-align:center;padding:3.5rem 0 2.5rem;position:relative}
.apple-logo-wrap{margin:0 auto 2rem;width:72px;height:72px}
.apple-svg{width:72px;height:72px;filter:drop-shadow(0 2px 12px rgba(0,0,0,0.10))}

h1{font-size:3rem;font-weight:200;letter-spacing:-1.5px;color:#1d1d1f;margin-bottom:0.3rem;line-height:1.1}
.role-line{font-size:13px;font-weight:400;letter-spacing:3px;color:#6e6e73;text-transform:uppercase;margin-bottom:1.6rem}
.pill-row{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin-bottom:1.6rem}
.pill{padding:6px 16px;border-radius:980px;font-size:12px;font-weight:400;background:rgba(0,0,0,0.05);color:#3a3a3c;border:0.5px solid rgba(0,0,0,0.08);letter-spacing:0.3px;transition:all 0.2s}
.pill:hover{background:rgba(0,0,0,0.09)}
.links-row{display:flex;gap:20px;justify-content:center;font-size:13px}
.links-row a{color:#0071e3;text-decoration:none;font-weight:400}
.links-row a:hover{text-decoration:underline}
.sep{color:#c7c7cc;font-size:11px}
.loc-line{margin-top:0.7rem;font-size:12px;color:#6e6e73;display:flex;align-items:center;gap:5px;justify-content:center}
.loc-dot{width:5px;height:5px;border-radius:50%;background:#34c759;display:inline-block}

.sec-head{font-size:11px;font-weight:500;letter-spacing:2.5px;color:#6e6e73;text-transform:uppercase;margin-bottom:1.1rem;margin-top:2.5rem;padding-bottom:0.5rem;border-bottom:0.5px solid rgba(0,0,0,0.08)}

.card{background:#fff;border-radius:18px;border:0.5px solid rgba(0,0,0,0.07);padding:1.4rem 1.5rem;transition:transform 0.2s}
.card:hover{transform:translateY(-1px)}
.g2{display:grid;grid-template-columns:1fr 1fr;gap:14px}
@media(max-width:540px){.g2{grid-template-columns:1fr}}
.card-ico{width:36px;height:36px;border-radius:9px;background:#f5f5f7;display:flex;align-items:center;justify-content:center;margin-bottom:0.9rem}
.card h3{font-size:14px;font-weight:500;color:#1d1d1f;margin-bottom:0.4rem;letter-spacing:-0.2px}
.card p{font-size:13px;color:#6e6e73;line-height:1.6;font-weight:300}

.skills-wrap{display:flex;flex-wrap:wrap;gap:8px;margin-top:0}
.sk{padding:7px 14px;border-radius:980px;font-size:12px;border:0.5px solid rgba(0,0,0,0.1);color:#3a3a3c;background:#fff;font-weight:400;letter-spacing:0.2px;display:flex;align-items:center;gap:6px}
.sk-dot{width:6px;height:6px;border-radius:50%}

.exp-card{background:#fff;border-radius:18px;border:0.5px solid rgba(0,0,0,0.07);padding:1.5rem;position:relative;overflow:hidden}
.exp-bar{position:absolute;left:0;top:0;bottom:0;width:2px;background:linear-gradient(to bottom,#0071e3,#34c759)}
.exp-role{font-size:15px;font-weight:500;color:#1d1d1f;letter-spacing:-0.3px}
.exp-co{font-size:13px;color:#0071e3;font-weight:400;margin:3px 0 2px}
.exp-date{font-size:11px;color:#6e6e73;margin-bottom:12px;display:flex;align-items:center;gap:4px}
.exp-date::before{content:'';width:4px;height:4px;border-radius:50%;background:#c7c7cc;display:inline-block}
.exp-items{list-style:none;display:flex;flex-direction:column;gap:6px}
.exp-items li{font-size:13px;color:#3a3a3c;font-weight:300;display:flex;gap:8px;align-items:flex-start;line-height:1.5}
.exp-items li::before{content:'';width:4px;height:4px;border-radius:50%;background:#0071e3;flex-shrink:0;margin-top:6px}
.hi{color:#1d1d1f;font-weight:500}

.proj-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px}
@media(max-width:540px){.proj-grid{grid-template-columns:1fr}}
.proj-card{background:#fff;border-radius:18px;border:0.5px solid rgba(0,0,0,0.07);padding:1.3rem 1.4rem;transition:transform 0.2s}
.proj-card:hover{transform:translateY(-1px)}
.proj-num{font-size:10px;font-weight:500;letter-spacing:2.5px;color:#0071e3;text-transform:uppercase;margin-bottom:0.5rem}
.proj-card h3{font-size:14px;font-weight:500;color:#1d1d1f;margin-bottom:0.4rem;letter-spacing:-0.2px}
.proj-card p{font-size:12px;color:#6e6e73;line-height:1.55;font-weight:300}
.tag-row{display:flex;flex-wrap:wrap;gap:5px;margin-top:10px}
.tag{font-size:10px;padding:3px 9px;border-radius:980px;background:#f5f5f7;border:0.5px solid rgba(0,0,0,0.08);color:#3a3a3c;font-weight:400}

.bot-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px}
@media(max-width:540px){.bot-grid{grid-template-columns:1fr}}
.edu-card,.cert-card{background:#fff;border-radius:18px;border:0.5px solid rgba(0,0,0,0.07);padding:1.3rem 1.4rem}
.edu-ico-wrap{width:38px;height:38px;border-radius:10px;background:#f5f5f7;display:flex;align-items:center;justify-content:center;margin-bottom:0.8rem}
.edu-deg{font-size:14px;font-weight:500;color:#1d1d1f;letter-spacing:-0.2px}
.edu-uni{font-size:12px;color:#0071e3;margin:2px 0}
.edu-yr{font-size:11px;color:#6e6e73}
.cert-item{display:flex;align-items:center;gap:10px;padding:8px 0;border-bottom:0.5px solid rgba(0,0,0,0.06)}
.cert-item:last-child{border-bottom:none;padding-bottom:0}
.cert-ico-box{width:30px;height:30px;border-radius:8px;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.cert-name{font-size:12px;font-weight:500;color:#1d1d1f}
.cert-org{font-size:11px;color:#6e6e73}

.stickers-row{display:flex;justify-content:center;gap:28px;margin-top:2.5rem;padding-bottom:1rem;flex-wrap:wrap}
.stk{animation:bob var(--s,3s) ease-in-out infinite alternate}
@keyframes bob{0%{transform:translateY(0) rotate(0deg)}100%{transform:translateY(-8px) rotate(4deg)}}

.footer{text-align:center;font-size:11px;color:#c7c7cc;letter-spacing:1.5px;margin-top:2rem;text-transform:uppercase}
</style>
</head>
<body>
<div class="wrap">

  <div class="hero">
    <div class="apple-logo-wrap">
      <svg class="apple-svg" viewBox="0 0 72 72" fill="none" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <linearGradient id="ag" x1="10" y1="8" x2="62" y2="68" gradientUnits="userSpaceOnUse">
            <stop offset="0%" stop-color="#555"/>
            <stop offset="50%" stop-color="#1d1d1f"/>
            <stop offset="100%" stop-color="#3a3a3c"/>
          </linearGradient>
        </defs>
        <path d="M48.5 10.5c.8-1 1.4-2.4 1.2-3.8-1.2.1-2.7.8-3.6 1.8-1 1-1.6 2.4-1.4 3.8 1.3.1 2.6-.7 3.8-1.8z" fill="url(#ag)"/>
        <path d="M50.4 13.2c-2.1-.1-3.9 1.2-4.9 1.2-1 0-2.6-1.1-4.3-1.1-2.2.1-4.3 1.3-5.4 3.3-2.3 4-.6 10 1.6 13.3 1.1 1.6 2.4 3.4 4.1 3.3 1.6-.1 2.2-1 4.1-1 1.9 0 2.5 1 4.2 1 1.8 0 2.9-1.6 4-3.2.7-1 1.2-2 1.6-3.1-4.2-1.6-4.9-7.7-.7-10.1-.9-1.6-2.4-3.5-4.3-3.6z" fill="url(#ag)"/>
      </svg>
    </div>
    <h1>Rohan</h1>
    <div class="role-line">Data Analyst &nbsp;·&nbsp; BI Developer &nbsp;·&nbsp; ML Engineer</div>
    <div class="pill-row">
      <span class="pill">Power BI</span>
      <span class="pill">Python</span>
      <span class="pill">MySQL</span>
      <span class="pill">Machine Learning</span>
      <span class="pill">AWS</span>
      <span class="pill">Deep Learning</span>
    </div>
    <div class="links-row">
      <a href="mailto:rohan2002cjj@gmail.com">Email</a>
      <span class="sep">·</span>
      <a href="https://www.linkedin.com/in/rohanjangir0/">LinkedIn</a>
      <span class="sep">·</span>
      <a href="https://github.com/rohancjj/">GitHub</a>
    </div>
    <div class="loc-line"><span class="loc-dot"></span>Hyderabad, India</div>
  </div>

  <div class="sec-head">About</div>
  <div class="g2">
    <div class="card">
      <div class="card-ico">
        <svg width="18" height="18" viewBox="0 0 18 18" fill="none"><circle cx="9" cy="9" r="7.5" stroke="#1d1d1f" stroke-width="1"/><path d="M9 5.5v3.5l2 2" stroke="#1d1d1f" stroke-width="1" stroke-linecap="round"/></svg>
      </div>
      <h3>Who I am</h3>
      <p>Data Analyst focused on turning raw data into meaningful insights using SQL, Power BI, Excel, and Python.</p>
    </div>
    <div class="card">
      <div class="card-ico">
        <svg width="18" height="18" viewBox="0 0 18 18" fill="none"><rect x="2.5" y="2.5" width="13" height="13" rx="3" stroke="#1d1d1f" stroke-width="1"/><path d="M6 9h6M9 6v6" stroke="#1d1d1f" stroke-width="1" stroke-linecap="round"/></svg>
      </div>
      <h3>What I do</h3>
      <p>I build end-to-end analytics pipelines — from data extraction to dashboards that drive decision-making.</p>
    </div>
  </div>

  <div class="sec-head">Skills</div>
  <div class="skills-wrap">
    <span class="sk"><span class="sk-dot" style="background:#0071e3"></span>MySQL</span>
    <span class="sk"><span class="sk-dot" style="background:#0071e3"></span>Excel</span>
    <span class="sk"><span class="sk-dot" style="background:#0071e3"></span>Power BI</span>
    <span class="sk"><span class="sk-dot" style="background:#34c759"></span>Pandas</span>
    <span class="sk"><span class="sk-dot" style="background:#34c759"></span>NumPy</span>
    <span class="sk"><span class="sk-dot" style="background:#34c759"></span>Matplotlib</span>
    <span class="sk"><span class="sk-dot" style="background:#34c759"></span>Seaborn</span>
    <span class="sk"><span class="sk-dot" style="background:#ff9f0a"></span>Scikit-learn</span>
    <span class="sk"><span class="sk-dot" style="background:#bf5af2"></span>ANN / CNN</span>
    <span class="sk"><span class="sk-dot" style="background:#bf5af2"></span>RNN</span>
    <span class="sk"><span class="sk-dot" style="background:#bf5af2"></span>Transformers</span>
  </div>

  <div class="sec-head">Experience</div>
  <div class="exp-card">
    <div class="exp-bar"></div>
    <div style="padding-left:12px">
      <div class="exp-role">Data Analyst Intern</div>
      <div class="exp-co">Hydizo Global Private Solutions · Hyderabad</div>
      <div class="exp-date">Sep – Dec 2024</div>
      <ul class="exp-items">
        <li>Extracted &amp; transformed business data using SQL</li>
        <li>Built Power BI dashboards for KPI tracking</li>
        <li>Improved performance by <span class="hi">35%+</span></li>
        <li>Automated recurring reports, saving hours of manual effort</li>
      </ul>
    </div>
  </div>

  <div class="sec-head">Projects</div>
  <div class="proj-grid">
    <div class="proj-card">
      <div class="proj-num">01 · Analytics</div>
      <h3>Business Health Analyzer</h3>
      <p>KPI-based system using SQL &amp; Power BI to classify business risk levels and surface critical signals.</p>
      <div class="tag-row"><span class="tag">SQL</span><span class="tag">Power BI</span><span class="tag">KPI</span></div>
    </div>
    <div class="proj-card">
      <div class="proj-num">02 · Machine Learning</div>
      <h3>Customer Segmentation</h3>
      <p>RFM-based segmentation to identify high-value and at-risk customers for targeted campaigns.</p>
      <div class="tag-row"><span class="tag">Python</span><span class="tag">RFM</span><span class="tag">Clustering</span></div>
    </div>
  </div>

  <div class="sec-head">Education &amp; Certifications</div>
  <div class="bot-grid">
    <div class="edu-card">
      <div class="edu-ico-wrap">
        <svg width="20" height="20" viewBox="0 0 20 20" fill="none"><path d="M10 2L2 7l8 5 8-5-8-5z" stroke="#1d1d1f" stroke-width="1" stroke-linejoin="round"/><path d="M4 8.5V14c0 1.1 2.7 3 6 3s6-1.9 6-3V8.5" stroke="#1d1d1f" stroke-width="1" stroke-linecap="round"/></svg>
      </div>
      <div class="edu-deg">B.Tech Computer Science</div>
      <div class="edu-uni">Amity University</div>
      <div class="edu-yr">2021 – 2025</div>
    </div>
    <div class="cert-card">
      <div class="cert-item">
        <div class="cert-ico-box" style="background:#fff3e0">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none"><rect x="1" y="3" width="14" height="10" rx="2" stroke="#ff9f0a" stroke-width="1"/><path d="M5 8h6M8 5v6" stroke="#ff9f0a" stroke-width="1" stroke-linecap="round"/></svg>
        </div>
        <div><div class="cert-name">Cloud Practitioner Essentials</div><div class="cert-org">Amazon Web Services</div></div>
      </div>
      <div class="cert-item">
        <div class="cert-ico-box" style="background:#e3f0ff">
          <svg width="16" height="16" viewBox="0 0 16 16" fill="none"><rect x="1" y="3" width="14" height="10" rx="2" stroke="#0071e3" stroke-width="1"/><path d="M4 8.5l2.5 2.5L12 6" stroke="#0071e3" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </div>
        <div><div class="cert-name">Power BI Data Analyst</div><div class="cert-org">Microsoft</div></div>
      </div>
    </div>
  </div>

  <div class="stickers-row">
    <svg style="--s:2.4s" class="stk" width="44" height="44" viewBox="0 0 44 44" fill="none">
      <circle cx="22" cy="22" r="20" fill="#f5f5f7" stroke="rgba(0,0,0,0.08)" stroke-width="0.5"/>
      <path d="M28 14.5c.6-.7 1-1.8.9-2.8-.9.1-2 .6-2.7 1.3-.7.8-1.2 1.8-1 2.8 1 .1 1.9-.5 2.8-1.3z" fill="#1d1d1f"/>
      <path d="M29.3 16.4c-1.6-.1-2.9.9-3.6.9-.8 0-1.9-.8-3.2-.8-1.6.1-3.2 1-4 2.5-1.7 3-.4 7.4 1.2 9.9.8 1.2 1.8 2.5 3 2.5 1.2-.1 1.6-.8 3-.8 1.4 0 1.8.8 3.1.8 1.3 0 2.2-1.2 3-2.4.5-.8.9-1.5 1.2-2.3-3.1-1.2-3.6-5.7-.5-7.5-.7-1.2-1.8-2.6-3.2-2.8z" fill="#1d1d1f"/>
    </svg>
    <svg style="--s:3s" class="stk" width="44" height="44" viewBox="0 0 44 44" fill="none">
      <circle cx="22" cy="22" r="20" fill="#f5f5f7" stroke="rgba(0,0,0,0.08)" stroke-width="0.5"/>
      <rect x="13" y="18" width="18" height="12" rx="2" stroke="#1d1d1f" stroke-width="1"/>
      <path d="M17 18v-2a5 5 0 0110 0v2" stroke="#1d1d1f" stroke-width="1" stroke-linecap="round"/>
      <circle cx="22" cy="24" r="2" fill="#1d1d1f"/>
    </svg>
    <svg style="--s:2.7s" class="stk" width="44" height="44" viewBox="0 0 44 44" fill="none">
      <circle cx="22" cy="22" r="20" fill="#f5f5f7" stroke="rgba(0,0,0,0.08)" stroke-width="0.5"/>
      <path d="M22 13l2.5 5 5.5.8-4 3.9.9 5.5L22 25.5l-4.9 2.7.9-5.5-4-3.9 5.5-.8L22 13z" stroke="#1d1d1f" stroke-width="1" stroke-linejoin="round" fill="none"/>
    </svg>
    <svg style="--s:3.4s" class="stk" width="44" height="44" viewBox="0 0 44 44" fill="none">
      <circle cx="22" cy="22" r="20" fill="#f5f5f7" stroke="rgba(0,0,0,0.08)" stroke-width="0.5"/>
      <ellipse cx="22" cy="23" rx="8" ry="6" stroke="#1d1d1f" stroke-width="1"/>
      <path d="M19 23c0-1.7 1.3-3 3-3" stroke="#1d1d1f" stroke-width="1" stroke-linecap="round"/>
      <circle cx="22" cy="23" r="1.5" fill="#1d1d1f"/>
      <path d="M22 14v2M22 30v2M14 23h2M28 23h2" stroke="#1d1d1f" stroke-width="1" stroke-linecap="round"/>
    </svg>
    <svg style="--s:2.2s" class="stk" width="44" height="44" viewBox="0 0 44 44" fill="none">
      <circle cx="22" cy="22" r="20" fill="#f5f5f7" stroke="rgba(0,0,0,0.08)" stroke-width="0.5"/>
      <rect x="14" y="14" width="16" height="16" rx="3" stroke="#1d1d1f" stroke-width="1"/>
      <path d="M17 20h10M17 24h6" stroke="#1d1d1f" stroke-width="1" stroke-linecap="round"/>
      <circle cx="28" cy="16" r="4" fill="#ff3b30"/>
      <path d="M27 16h2M28 15v2" stroke="#fff" stroke-width="0.8" stroke-linecap="round"/>
    </svg>
  </div>

  <div class="footer">Designed with clarity &nbsp;·&nbsp; Rohan · 2025</div>
</div>
</body>
</html>
