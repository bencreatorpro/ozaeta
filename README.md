<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ben.supply — Packages</title>
<link href="https://fonts.googleapis.com/css2?family=Exo+2:wght@600;700;800;900&family=Inter:wght@300;400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg:             #080809;
  --surface:        #0F0F11;
  --card:           #141416;
  --card-2:         #1A1A1D;
  --card-3:         #202024;
  --border:         rgba(255,255,255,0.07);
  --border-2:       rgba(255,255,255,0.13);
  --white:          #F3F3F4;
  --grey-1:         #9A9AA4;
  --grey-2:         #4E4E58;
  --grey-3:         #252529;
  --green:          #2ECC8A;
  --green-soft:     rgba(46,204,138,0.09);
  --green-border:   rgba(46,204,138,0.25);
  --green-dim:      rgba(46,204,138,0.55);
  --orange:         #E8722A;
  --orange-soft:    rgba(232,114,42,0.09);
  --orange-border:  rgba(232,114,42,0.28);
  --radius:         20px;
  --radius-sm:      11px;
  --radius-xs:      6px;
  --gap:            20px;
}

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--white);
  font-family: 'Inter', sans-serif;
  font-size: 13px;
  line-height: 1.7;
  -webkit-font-smoothing: antialiased;
}

/* ─── DISPLAY FONT ─── */
.display {
  font-family: 'Exo 2', sans-serif;
}

.mono {
  font-family: 'IBM Plex Mono', monospace;
}

/* ─── LABEL ─── */
.label-xs {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 9px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--grey-2);
}

/* ─── SHELL ─── */
.shell {
  max-width: 1080px;
  margin: 0 auto;
  padding: 48px 40px 100px;
}

/* ─── TOPBAR ─── */
.topbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 40px;
  border-bottom: 1px solid var(--border);
  margin-bottom: 64px;
}

.logo {
  font-family: 'Exo 2', sans-serif;
  font-size: 16px;
  font-weight: 800;
  color: var(--white);
  letter-spacing: -0.01em;
}

.logo span { color: var(--green); }

.topbar-meta {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10px;
  color: var(--grey-2);
  letter-spacing: 0.12em;
  text-transform: uppercase;
}

/* ─── HERO ─── */
.hero {
  display: grid;
  grid-template-columns: 1fr 380px;
  gap: 40px;
  align-items: start;
  margin-bottom: 80px;
}

.hero-title {
  font-family: 'Exo 2', sans-serif;
  font-size: 76px;
  font-weight: 900;
  line-height: 0.88;
  letter-spacing: -0.03em;
  color: var(--white);
}

.hero-title em {
  font-style: normal;
  color: var(--green);
}

.hero-sub {
  font-size: 14px;
  color: var(--grey-1);
  line-height: 1.9;
  margin-top: 24px;
  font-weight: 400;
  max-width: 420px;
}

/* ─── ROI CARD ─── */
.roi-card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  overflow: hidden;
}

.roi-card-top {
  padding: 18px 24px;
  border-bottom: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.roi-card-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 9px;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--grey-2);
}

.live-dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: var(--green);
  box-shadow: 0 0 10px var(--green);
}

.roi-scenario {
  padding: 18px 24px;
  background: var(--green-soft);
  border-bottom: 1px solid var(--green-border);
}

.roi-scenario-tag {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 9px;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--green-dim);
  margin-bottom: 5px;
}

.roi-scenario-name {
  font-size: 13px;
  font-weight: 600;
  color: var(--white);
}

.roi-scenario-goal {
  font-size: 12px;
  color: var(--grey-1);
  margin-top: 2px;
}

.roi-rows { padding: 6px 0; }

.roi-row {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 12px 24px;
  border-bottom: 1px solid var(--border);
}

.roi-row:last-child { border-bottom: none; }

.roi-row-label { font-size: 12px; color: var(--grey-1); font-weight: 400; }

.roi-row-val { font-weight: 700; font-size: 14px; color: var(--white); }
.roi-row-val.green { color: var(--green); }
.roi-row-val.orange { color: var(--orange); }

.roi-foot {
  padding: 16px 24px;
  background: var(--orange-soft);
  border-top: 1px solid var(--orange-border);
}

.roi-foot-text {
  font-size: 11px;
  color: var(--grey-1);
  line-height: 1.7;
}

.roi-foot-text strong { color: var(--white); }

/* ─── SECTION DIVIDER ─── */
.divider {
  display: flex;
  align-items: center;
  gap: 16px;
  margin: 0 0 32px;
}

.divider-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 9px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--grey-2);
  white-space: nowrap;
}

.divider-line {
  flex: 1;
  height: 1px;
  background: var(--border);
}

/* ─── PACKAGES ─── */
.packages {
  display: flex;
  flex-direction: column;
  gap: var(--gap);
}

.pkg-card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  overflow: hidden;
  transition: border-color 0.25s;
}

.pkg-card:hover { border-color: var(--border-2); }
.pkg-card.addon { border-color: var(--orange-border); }
.pkg-card.addon:hover { border-color: rgba(232,114,42,0.5); }

/* PKG HEADER */
.pkg-hd {
  padding: 36px 40px 28px;
  border-bottom: 1px solid var(--border);
}

.pkg-eyebrow {
  display: flex;
  align-items: center;
  gap: 10px;
  margin-bottom: 16px;
  flex-wrap: wrap;
}

.badge {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 9px;
  letter-spacing: 0.13em;
  text-transform: uppercase;
  padding: 4px 10px;
  border-radius: var(--radius-xs);
}

.badge-default {
  color: var(--grey-2);
  background: var(--card-2);
  border: 1px solid var(--border);
}

.badge-green {
  color: var(--green-dim);
  background: var(--green-soft);
  border: 1px solid var(--green-border);
}

.badge-orange {
  color: var(--orange);
  background: var(--orange-soft);
  border: 1px solid var(--orange-border);
}

.badge-includes {
  color: var(--grey-2);
  background: transparent;
  border: none;
  padding-left: 0;
}

.pkg-name {
  font-family: 'Exo 2', sans-serif;
  font-size: 42px;
  font-weight: 900;
  letter-spacing: -0.02em;
  line-height: 1;
  color: var(--white);
  margin-bottom: 14px;
}

.pkg-tagline {
  font-size: 13px;
  color: var(--grey-1);
  font-style: italic;
  line-height: 1.6;
  font-weight: 400;
  max-width: 540px;
}

/* PKG BODY */
.pkg-body {
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.pkg-col {
  padding: 32px 40px;
}

.pkg-col + .pkg-col {
  border-left: 1px solid var(--border);
}

.pkg-col-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 9px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--grey-2);
  margin-bottom: 18px;
  padding-bottom: 12px;
  border-bottom: 1px solid var(--border);
}

.pkg-what {
  font-size: 13px;
  color: var(--grey-1);
  line-height: 1.9;
  font-weight: 400;
}

.pkg-what strong { color: var(--white); font-weight: 600; }

.d-list { list-style: none; }

.d-item {
  display: grid;
  grid-template-columns: 8px 1fr;
  gap: 14px;
  padding: 12px 0;
  border-bottom: 1px solid var(--border);
  align-items: start;
}

.d-item:last-child { border-bottom: none; }

.d-dot {
  width: 5px;
  height: 5px;
  border-radius: 50%;
  background: var(--green);
  margin-top: 7px;
  flex-shrink: 0;
}

.d-name {
  font-size: 13px;
  font-weight: 600;
  color: var(--white);
  margin-bottom: 4px;
}

.d-subs { margin-top: 4px; }

.d-sub {
  font-size: 11px;
  color: var(--grey-2);
  line-height: 1.5;
  padding-left: 10px;
  position: relative;
}

.d-sub::before { content: '·'; position: absolute; left: 1px; color: var(--grey-3); }

/* PKG FOOTER */
.pkg-ft {
  border-top: 1px solid var(--border);
  padding: 24px 40px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: var(--card-2);
  gap: 24px;
  flex-wrap: wrap;
}

.pkg-ft.addon-ft {
  background: var(--orange-soft);
  border-top-color: var(--orange-border);
}

.ft-left {}

.ft-price-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 9px;
  letter-spacing: 0.15em;
  text-transform: uppercase;
  color: var(--grey-2);
  margin-bottom: 4px;
}

.ft-price {
  font-family: 'Exo 2', sans-serif;
  font-size: 38px;
  font-weight: 900;
  letter-spacing: -0.03em;
  color: var(--white);
  line-height: 1;
}

.ft-price.free { font-size: 26px; color: var(--grey-2); font-weight: 600; font-family: 'Inter', sans-serif; }
.ft-price.orange { color: var(--orange); }

.ft-note {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10px;
  color: var(--grey-2);
  margin-top: 5px;
}

.ft-right {
  display: flex;
  align-items: center;
  gap: 10px;
  flex-shrink: 0;
  flex-wrap: wrap;
}

/* ─── BUTTONS ─── */
.btn {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  font-family: 'Inter', sans-serif;
  font-size: 13px;
  font-weight: 600;
  padding: 13px 22px;
  border-radius: var(--radius-sm);
  text-decoration: none;
  border: none;
  cursor: pointer;
  transition: opacity 0.18s, transform 0.15s;
  letter-spacing: -0.01em;
  white-space: nowrap;
}

.btn:hover { opacity: 0.85; transform: translateY(-1px); }

.btn-download {
  background: var(--green);
  color: #050F09;
}

.btn-deposit {
  background: transparent;
  color: var(--grey-1);
  border: 1px solid var(--border-2);
}

.btn-deposit:hover { background: var(--card-3); color: var(--white); opacity: 1; }

.btn-full {
  background: var(--orange);
  color: #fff;
}

.btn-full-green {
  background: var(--green);
  color: #050F09;
}

.btn svg {
  width: 15px;
  height: 15px;
  flex-shrink: 0;
}

/* Download icon */
.ico-download { fill: none; stroke: currentColor; stroke-width: 2; stroke-linecap: round; stroke-linejoin: round; }

/* PayPal icon */
.ico-pp { fill: rgba(255,255,255,0.85); }
.ico-pp-dark { fill: rgba(5,15,9,0.7); }

.discount-tag {
  font-size: 10px;
  color: var(--green-dim);
  font-weight: 500;
  white-space: nowrap;
}

/* ─── BOTTOM GRID ─── */
.bottom-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: var(--gap);
  margin-top: var(--gap);
}

.bottom-card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 40px;
}

.bc-label {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 9px;
  letter-spacing: 0.2em;
  text-transform: uppercase;
  color: var(--green-dim);
  margin-bottom: 16px;
}

.bc-title {
  font-family: 'Exo 2', sans-serif;
  font-size: 32px;
  font-weight: 900;
  letter-spacing: -0.02em;
  line-height: 1;
  color: var(--white);
  margin-bottom: 20px;
}

.bc-text {
  font-size: 13px;
  color: var(--grey-1);
  line-height: 1.9;
}

.bc-text strong { color: var(--white); font-weight: 600; }

.pay-list { list-style: none; }

.pay-item {
  display: grid;
  grid-template-columns: 8px 1fr;
  gap: 14px;
  padding: 14px 0;
  border-bottom: 1px solid var(--border);
  align-items: start;
}

.pay-item:last-child { border-bottom: none; }

.pay-name { font-size: 13px; font-weight: 600; color: var(--white); margin-bottom: 3px; }
.pay-detail { font-size: 11px; color: var(--grey-2); line-height: 1.6; }

/* ─── CLOSE ─── */
.close-strip {
  margin-top: var(--gap);
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  padding: 52px 56px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 40px;
}

.close-title {
  font-family: 'Exo 2', sans-serif;
  font-size: 56px;
  font-weight: 900;
  letter-spacing: -0.03em;
  line-height: 0.92;
  color: var(--white);
}

.close-title em { font-style: normal; color: var(--green); }

.close-right { text-align: right; flex-shrink: 0; }

.close-cta {
  font-size: 13px;
  color: var(--grey-1);
  line-height: 1.9;
  margin-bottom: 20px;
}

.close-cta strong { color: var(--white); font-weight: 600; }

.close-brand {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10px;
  color: var(--grey-2);
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

/* ─── FOOTER ─── */
.footer {
  margin-top: 48px;
  padding-top: 24px;
  border-top: 1px solid var(--border);
  display: flex;
  justify-content: space-between;
}

.footer-text {
  font-family: 'IBM Plex Mono', monospace;
  font-size: 10px;
  color: var(--grey-2);
  letter-spacing: 0.1em;
  text-transform: uppercase;
}

</style>
</head>
<body>
<div class="shell">

  <!-- TOPBAR -->
  <div class="topbar">
    <div class="logo">ben<span>.</span>supply</div>
    <div class="topbar-meta">Packages — 2026</div>
  </div>

  <!-- HERO -->
  <div class="hero">
    <div>
      <div class="hero-title">Build.<br>Launch.<br><em>Win.</em></div>
      <div class="hero-sub">
        Four packages. One direction —<br>
        from zero to results.<br>
        Start with The Blueprint. It's free.
      </div>
    </div>

    <div class="roi-card">
      <div class="roi-card-top">
        <div class="roi-card-label">Client ROI Scenario</div>
        <div class="live-dot"></div>
      </div>
      <div class="roi-scenario">
        <div class="roi-scenario-tag">Client</div>
        <div class="roi-scenario-name">Marty Ozaeta — Fitness Coach</div>
        <div class="roi-scenario-goal">Goal: $175,000 in 6 months post-launch</div>
      </div>
      <div class="roi-rows">
        <div class="roi-row">
          <div class="roi-row-label">6-month revenue goal</div>
          <div class="roi-row-val green">$175,000</div>
        </div>
        <div class="roi-row">
          <div class="roi-row-label">Full brand identity cost</div>
          <div class="roi-row-val orange">$20,000</div>
        </div>
        <div class="roi-row">
          <div class="roi-row-label">Brand as % of goal</div>
          <div class="roi-row-val">~11.4%</div>
        </div>
        <div class="roi-row">
          <div class="roi-row-label">Net return (if goal hit)</div>
          <div class="roi-row-val green">$155,000</div>
        </div>
      </div>
      <div class="roi-foot">
        <div class="roi-foot-text">
          <strong>$20k in. $175k out.</strong><br>
          The brand isn't the cost — going unnoticed is.
        </div>
      </div>
    </div>
  </div>

  <!-- THE OFFER -->
  <div class="divider">
    <div class="divider-label">The Offer</div>
    <div class="divider-line"></div>
  </div>

  <div class="packages">

    <!-- ── PACKAGE 01 ── -->
    <div class="pkg-card">
      <div class="pkg-hd">
        <div class="pkg-eyebrow">
          <div class="badge badge-default">Package 01</div>
          <div class="badge badge-green">Complimentary</div>
        </div>
        <div class="pkg-name">The Blueprint</div>
        <div class="pkg-tagline">"We define and plan for you, so that you're not drifting — you're intentional."</div>
      </div>

      <div class="pkg-body">
        <div class="pkg-col">
          <div class="pkg-col-label">What it is</div>
          <div class="pkg-what">
            A complete brand strategy, creative direction, and initial concepts — researched, built, and <strong>provided to you at no cost</strong>.<br><br>
            You leave with a clear picture of your brand, your market, and the full creative vision for everything we'll build together.
          </div>
        </div>
        <div class="pkg-col">
          <div class="pkg-col-label">What you get</div>
          <ul class="d-list">
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">Brand Strategy</div>
                <div class="d-subs">
                  <div class="d-sub">Positioning — where you stand in the market</div>
                  <div class="d-sub">Brand story — the narrative that attracts clients</div>
                  <div class="d-sub">Target audience — who you're built for</div>
                </div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">Creative Direction</div>
                <div class="d-subs">
                  <div class="d-sub">Visual and verbal brand direction</div>
                  <div class="d-sub">Initial concepts for every deliverable</div>
                </div>
              </div>
            </li>
          </ul>
        </div>
      </div>

      <div class="pkg-ft">
        <div class="ft-left">
          <div class="ft-price-label">Funding</div>
          <div class="ft-price free">Complimentary</div>
          <div class="ft-note">Delivered at first presentation</div>
        </div>
        <div class="ft-right">
          <a href="https://drive.google.com/PLACEHOLDER_BLUEPRINT_LINK" class="btn btn-download" target="_blank">
            <svg viewBox="0 0 24 24" width="15" height="15">
              <polyline class="ico-download" points="8 17 12 21 16 17"/>
              <line class="ico-download" x1="12" y1="12" x2="12" y2="21"/>
              <path class="ico-download" d="M20.88 18.09A5 5 0 0 0 18 9h-1.26A8 8 0 1 0 3 16.29"/>
            </svg>
            Download Blueprint — Free
          </a>
        </div>
      </div>
    </div>

    <!-- ── PACKAGE 02 ── -->
    <div class="pkg-card">
      <div class="pkg-hd">
        <div class="pkg-eyebrow">
          <div class="badge badge-default">Package 02</div>
          <div class="badge badge-includes">Includes Package 01</div>
        </div>
        <div class="pkg-name">The Brand</div>
        <div class="pkg-tagline">"We build and deliver for you, so that you don't wing it — you own it."</div>
      </div>

      <div class="pkg-body">
        <div class="pkg-col">
          <div class="pkg-col-label">What it is</div>
          <div class="pkg-what">
            Your brand, built from the ground up and delivered ready to use. Every asset you need to <strong>show up with authority</strong> — online, in person, and in front of the clients you want.<br><br>
            Professional. Distinctive. Yours.
          </div>
        </div>
        <div class="pkg-col">
          <div class="pkg-col-label">What you get</div>
          <ul class="d-list">
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">Brand Identity</div>
                <div class="d-subs">
                  <div class="d-sub">Name + tagline</div>
                  <div class="d-sub">Logo suite — primary, secondary, icon</div>
                  <div class="d-sub">Colour palette + typography system</div>
                </div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">3 Brand Applications</div>
                <div class="d-subs"><div class="d-sub">Social, print, and digital</div></div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">Landing Page</div>
                <div class="d-subs"><div class="d-sub">Designed and built to convert</div></div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">Full Asset Delivery</div>
                <div class="d-subs"><div class="d-sub">All files packaged and delivered</div></div>
              </div>
            </li>
          </ul>
        </div>
      </div>

      <div class="pkg-ft">
        <div class="ft-left">
          <div class="ft-price-label">Funding</div>
          <div class="ft-price">$10,000</div>
          <div class="ft-note">2 weeks delivery</div>
        </div>
        <div class="ft-right">
          <a href="https://paypal.com/pay/PLACEHOLDER_PKG02_DEPOSIT" class="btn btn-deposit" target="_blank">
            Pay deposit — $5,000
          </a>
          <a href="https://paypal.com/pay/PLACEHOLDER_PKG02_FULL" class="btn btn-full" target="_blank">
            <svg viewBox="0 0 24 24" width="15" height="15"><path class="ico-pp" d="M20.067 8.478c.492.88.556 2.014.3 3.327-.74 3.806-3.276 5.12-6.514 5.12h-.5a.805.805 0 0 0-.794.68l-.04.22-.63 3.993-.032.17a.804.804 0 0 1-.794.679H8.585a.468.468 0 0 1-.464-.543l.993-6.268A.805.805 0 0 1 9.9 14.6h1.396c3.455 0 6.161-1.404 6.953-5.464.332-1.696.16-3.108-.556-4.103a4.02 4.02 0 0 0-1.154-.955 6.655 6.655 0 0 1 1.54.604c.735.426 1.584 1.217 1.988 3.796z"/><path class="ico-pp" d="M18.163 4.717c-.505-.248-1.067-.42-1.677-.514-.61-.093-1.277-.135-1.993-.135H9.195a.805.805 0 0 0-.794.679L7.04 14.297a.468.468 0 0 0 .463.543h3.062l.768-4.876.024-.153a.805.805 0 0 1 .794-.679h1.654c3.237 0 5.773-1.315 6.513-5.12.022-.112.041-.221.057-.329a4.63 4.63 0 0 0-.84-.634 4.715 4.715 0 0 0-.372-.332z"/></svg>
            Pay in full (20% off) — $8,000
          </a>
        </div>
      </div>
    </div>

    <!-- ── PACKAGE 03 ── -->
    <div class="pkg-card">
      <div class="pkg-hd">
        <div class="pkg-eyebrow">
          <div class="badge badge-default">Package 03</div>
          <div class="badge badge-includes">Includes Packages 01 + 02</div>
        </div>
        <div class="pkg-name">The Execution</div>
        <div class="pkg-tagline">"We market and launch for you, so that you don't go unnoticed — you get found."</div>
      </div>

      <div class="pkg-body">
        <div class="pkg-col">
          <div class="pkg-col-label">What it is</div>
          <div class="pkg-what">
            Your brand, live and in front of the right people. We take everything built in The Brand and put it to work — full marketing strategy, content, and a complete campaign launch behind it.<br><br>
            <strong>You don't just have a brand. You have momentum.</strong>
          </div>
        </div>
        <div class="pkg-col">
          <div class="pkg-col-label">What you get</div>
          <ul class="d-list">
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">Marketing Strategy</div>
                <div class="d-subs"><div class="d-sub">Channel selection, messaging, and targeting</div></div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">Content + Assets</div>
                <div class="d-subs"><div class="d-sub">Launch content produced and ready</div></div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">Campaign Launch</div>
                <div class="d-subs"><div class="d-sub">Full deployment across chosen channels</div></div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot"></div>
              <div>
                <div class="d-name">Performance Reports</div>
                <div class="d-subs"><div class="d-sub">7-day pulse + 30-day full report</div></div>
              </div>
            </li>
          </ul>
        </div>
      </div>

      <div class="pkg-ft">
        <div class="ft-left">
          <div class="ft-price-label">Funding</div>
          <div class="ft-price">$20,000</div>
          <div class="ft-note">2 weeks post brand delivery</div>
        </div>
        <div class="ft-right">
          <a href="https://paypal.com/pay/PLACEHOLDER_PKG03_DEPOSIT" class="btn btn-deposit" target="_blank">
            Pay deposit — $10,000
          </a>
          <a href="https://paypal.com/pay/PLACEHOLDER_PKG03_FULL" class="btn btn-full" target="_blank">
            <svg viewBox="0 0 24 24" width="15" height="15"><path class="ico-pp" d="M20.067 8.478c.492.88.556 2.014.3 3.327-.74 3.806-3.276 5.12-6.514 5.12h-.5a.805.805 0 0 0-.794.68l-.04.22-.63 3.993-.032.17a.804.804 0 0 1-.794.679H8.585a.468.468 0 0 1-.464-.543l.993-6.268A.805.805 0 0 1 9.9 14.6h1.396c3.455 0 6.161-1.404 6.953-5.464.332-1.696.16-3.108-.556-4.103a4.02 4.02 0 0 0-1.154-.955 6.655 6.655 0 0 1 1.54.604c.735.426 1.584 1.217 1.988 3.796z"/><path class="ico-pp" d="M18.163 4.717c-.505-.248-1.067-.42-1.677-.514-.61-.093-1.277-.135-1.993-.135H9.195a.805.805 0 0 0-.794.679L7.04 14.297a.468.468 0 0 0 .463.543h3.062l.768-4.876.024-.153a.805.805 0 0 1 .794-.679h1.654c3.237 0 5.773-1.315 6.513-5.12.022-.112.041-.221.057-.329a4.63 4.63 0 0 0-.84-.634 4.715 4.715 0 0 0-.372-.332z"/></svg>
            Pay in full (20% off) — $16,000
          </a>
        </div>
      </div>
    </div>

    <!-- ── THE RESULTS ── -->
    <div class="pkg-card addon">
      <div class="pkg-hd">
        <div class="pkg-eyebrow">
          <div class="badge badge-orange">Add-On</div>
          <div class="badge badge-includes">Available with any package</div>
        </div>
        <div class="pkg-name">The Results</div>
        <div class="pkg-tagline">"We optimise and grow for you, so that you don't plateau — you compound."</div>
      </div>

      <div class="pkg-body">
        <div class="pkg-col">
          <div class="pkg-col-label">What it is</div>
          <div class="pkg-what">
            We don't launch and leave. An ongoing engagement where we stay in the work with you — <strong>optimising, growing, and driving results</strong> on a quarterly basis for as long as you want to compete.
          </div>
        </div>
        <div class="pkg-col">
          <div class="pkg-col-label">What you get</div>
          <ul class="d-list">
            <li class="d-item">
              <div class="d-dot" style="background:var(--orange);"></div>
              <div>
                <div class="d-name">Monthly Growth Cycle</div>
                <div class="d-subs"><div class="d-sub">Ongoing content and campaign management</div></div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot" style="background:var(--orange);"></div>
              <div>
                <div class="d-name">Monthly Performance Report</div>
                <div class="d-subs"><div class="d-sub">Data, insights, and next actions</div></div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot" style="background:var(--orange);"></div>
              <div>
                <div class="d-name">Quarterly Check-In with Ben</div>
                <div class="d-subs"><div class="d-sub">Results, direction, and next quarter planning</div></div>
              </div>
            </li>
            <li class="d-item">
              <div class="d-dot" style="background:var(--orange);"></div>
              <div>
                <div class="d-name">Priority Access</div>
                <div class="d-subs"><div class="d-sub">Direct line, fast response, first availability</div></div>
              </div>
            </li>
          </ul>
        </div>
      </div>

      <div class="pkg-ft addon-ft">
        <div class="ft-left">
          <div class="ft-price-label">Funding</div>
          <div class="ft-price orange">$3,000 / quarter</div>
          <div class="ft-note">3-month blocks — cancel before next cycle, no penalty</div>
        </div>
        <div class="ft-right">
          <a href="https://paypal.com/pay/PLACEHOLDER_RESULTS_DEPOSIT" class="btn btn-deposit" target="_blank">
            Pay deposit — $1,500
          </a>
          <a href="https://paypal.com/pay/PLACEHOLDER_RESULTS_FULL" class="btn btn-full" target="_blank">
            <svg viewBox="0 0 24 24" width="15" height="15"><path class="ico-pp" d="M20.067 8.478c.492.88.556 2.014.3 3.327-.74 3.806-3.276 5.12-6.514 5.12h-.5a.805.805 0 0 0-.794.68l-.04.22-.63 3.993-.032.17a.804.804 0 0 1-.794.679H8.585a.468.468 0 0 1-.464-.543l.993-6.268A.805.805 0 0 1 9.9 14.6h1.396c3.455 0 6.161-1.404 6.953-5.464.332-1.696.16-3.108-.556-4.103a4.02 4.02 0 0 0-1.154-.955 6.655 6.655 0 0 1 1.54.604c.735.426 1.584 1.217 1.988 3.796z"/><path class="ico-pp" d="M18.163 4.717c-.505-.248-1.067-.42-1.677-.514-.61-.093-1.277-.135-1.993-.135H9.195a.805.805 0 0 0-.794.679L7.04 14.297a.468.468 0 0 0 .463.543h3.062l.768-4.876.024-.153a.805.805 0 0 1 .794-.679h1.654c3.237 0 5.773-1.315 6.513-5.12.022-.112.041-.221.057-.329a4.63 4.63 0 0 0-.84-.634 4.715 4.715 0 0 0-.372-.332z"/></svg>
            Pay in full (20% off) — $2,400
          </a>
        </div>
      </div>
    </div>

  </div>

  <!-- TERMS -->
  <div class="divider" style="margin-top:48px;">
    <div class="divider-label">Terms</div>
    <div class="divider-line"></div>
  </div>

  <div class="bottom-grid">
    <div class="bottom-card">
      <div class="bc-label">The Guarantee</div>
      <div class="bc-title">We deliver.<br>Full stop.</div>
      <div class="bc-text">
        If we don't deliver everything promised to the standard agreed — <strong>we work for free until we do.</strong><br><br>
        No exceptions. Full terms confirmed at sign-off.
      </div>
    </div>

    <div class="bottom-card">
      <div class="bc-label">Payment</div>
      <div class="bc-title">Simple.<br>Clear.</div>
      <ul class="pay-list">
        <li class="pay-item">
          <div class="d-dot"></div>
          <div>
            <div class="pay-name">Packages 02 + 03</div>
            <div class="pay-detail">50% deposit to begin. 50% on final delivery. Or save 20% paying in full.</div>
          </div>
        </li>
        <li class="pay-item">
          <div class="d-dot"></div>
          <div>
            <div class="pay-name">The Results</div>
            <div class="pay-detail">$1,500 deposit or $2,400 quarterly in full (20% off). Cancel before next cycle — no penalty.</div>
          </div>
        </li>
        <li class="pay-item">
          <div class="d-dot"></div>
          <div>
            <div class="pay-name">Method</div>
            <div class="pay-detail">PayPal. Payment links on each package above.</div>
          </div>
        </li>
      </ul>
    </div>
  </div>

  <!-- CLOSE -->
  <div class="close-strip">
    <div class="close-title">Ready<br>to <em>win?</em></div>
    <div class="close-right">
      <div class="close-cta">
        Start with The Blueprint — <strong>it's free.</strong><br>
        One conversation is all it takes.
      </div>
      <div class="close-brand">ben.supply — Building brands that mean business.</div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-text">ben.supply</div>
    <div class="footer-text">2026</div>
  </div>

</div>
</body>
</html>
