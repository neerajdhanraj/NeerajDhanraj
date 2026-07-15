---
layout: default
title: VedicDateTime
permalink: /vedicdatetime/
---

<style>
  :root {
    --vdt-bg: #fcfbf7;
    --vdt-surface: #ffffff;
    --vdt-surface-2: #f7f3ea;
    --vdt-text: #1f2937;
    --vdt-muted: #6b7280;
    --vdt-border: #e5dcc7;
    --vdt-primary: #b7791f;
    --vdt-primary-2: #d4a017;
    --vdt-accent: #8b5e34;
    --vdt-success: #0f766e;
    --vdt-shadow: 0 10px 30px rgba(120, 90, 40, 0.08);
    --vdt-radius: 20px;
    --vdt-max: 1180px;
  }

  .vdt-page * { box-sizing: border-box; }
  .vdt-page {
    background: linear-gradient(180deg, #fffdf8 0%, #fcfbf7 100%);
    color: var(--vdt-text);
    margin: 0 auto;
    padding: 2rem 1rem 4rem;
    font-family: inherit;
  }
  .vdt-wrap {
    max-width: var(--vdt-max);
    margin: 0 auto;
  }
  .vdt-section {
    margin-top: 2rem;
  }
  .vdt-card {
    background: var(--vdt-surface);
    border: 1px solid var(--vdt-border);
    border-radius: var(--vdt-radius);
    box-shadow: var(--vdt-shadow);
  }
  .vdt-hero {
    position: relative;
    overflow: hidden;
    padding: 2rem;
    background:
      radial-gradient(circle at top right, rgba(212,160,23,0.14), transparent 28%),
      radial-gradient(circle at left center, rgba(183,121,31,0.12), transparent 20%),
      linear-gradient(135deg, #fffdfa 0%, #f8f4ea 100%);
  }
  .vdt-hero-grid {
    display: grid;
    grid-template-columns: 160px 1fr;
    gap: 1.75rem;
    align-items: center;
  }
  .vdt-logo-box {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .vdt-logo {
    width: 100%;
    max-width: 150px;
    height: auto;
    display: block;
    filter: drop-shadow(0 10px 18px rgba(122, 84, 24, 0.16));
  }
  .vdt-kicker {
    display: inline-block;
    font-size: 0.78rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    color: var(--vdt-accent);
    background: rgba(183,121,31,0.08);
    padding: 0.35rem 0.7rem;
    border-radius: 999px;
    margin-bottom: 0.9rem;
    font-weight: 700;
  }
  .vdt-title {
    margin: 0;
    font-size: clamp(2rem, 4vw, 3.4rem);
    line-height: 1.05;
    color: #3f2b12;
  }
  .vdt-subtitle {
    margin: 0.9rem 0 1rem;
    max-width: 760px;
    font-size: 1.05rem;
    line-height: 1.7;
    color: #4b5563;
  }
  .vdt-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8rem;
    margin-top: 1.25rem;
  }
  .vdt-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    min-height: 44px;
    padding: 0.78rem 1.05rem;
    border-radius: 12px;
    border: 1px solid transparent;
    text-decoration: none;
    font-weight: 700;
    transition: 0.2s ease;
    cursor: pointer;
  }
  .vdt-btn-primary {
    background: linear-gradient(135deg, var(--vdt-primary), var(--vdt-primary-2));
    color: #fff;
  }
  .vdt-btn-secondary {
    background: #fff;
    border-color: var(--vdt-border);
    color: var(--vdt-text);
  }
  .vdt-btn:hover {
    transform: translateY(-1px);
    box-shadow: 0 10px 20px rgba(120, 90, 40, 0.12);
  }

  .vdt-stat-grid,
  .vdt-feature-grid,
  .vdt-meta-grid,
  .vdt-links-grid {
    display: grid;
    gap: 1rem;
  }
  .vdt-stat-grid {
    grid-template-columns: repeat(4, minmax(0, 1fr));
    margin-top: 1.5rem;
  }
  .vdt-stat {
    padding: 1rem 1.1rem;
    border-radius: 16px;
    background: rgba(255,255,255,0.78);
    border: 1px solid rgba(229,220,199,0.9);
  }
  .vdt-stat strong {
    display: block;
    font-size: 1.3rem;
    color: var(--vdt-primary);
  }
  .vdt-stat span {
    color: var(--vdt-muted);
    font-size: 0.95rem;
  }

  .vdt-section-head {
    margin-bottom: 1rem;
  }
  .vdt-section-head h2 {
    margin: 0;
    font-size: clamp(1.45rem, 2vw, 2rem);
    color: #3f2b12;
  }
  .vdt-section-head p {
    margin: 0.5rem 0 0;
    color: var(--vdt-muted);
    line-height: 1.7;
  }

  .vdt-overview {
    padding: 1.5rem;
  }

  .vdt-meta-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
    margin-top: 1rem;
  }
  .vdt-meta-item {
    padding: 1rem;
    border: 1px solid var(--vdt-border);
    border-radius: 16px;
    background: linear-gradient(180deg, #fff 0%, #fbf8f1 100%);
  }
  .vdt-meta-item .label {
    display: block;
    font-size: 0.78rem;
    text-transform: uppercase;
    letter-spacing: 0.06em;
    color: var(--vdt-muted);
    margin-bottom: 0.35rem;
  }
  .vdt-meta-item .value {
    font-weight: 600;
    line-height: 1.55;
  }

  .vdt-console {
    margin-top: 1.4rem;
    border-radius: 18px;
    overflow: hidden;
    border: 1px solid #d6c7a8;
    box-shadow: 0 16px 40px rgba(87, 64, 25, 0.12);
  }
  .vdt-console-bar {
    display: flex;
    align-items: center;
    gap: 0.45rem;
    padding: 0.7rem 1rem;
    background: linear-gradient(180deg, #3e2c16 0%, #2a1f12 100%);
  }
  .vdt-console-dot {
    width: 11px;
    height: 11px;
    border-radius: 50%;
    display: inline-block;
  }
  .vdt-console-dot.red { background: #ff5f57; }
  .vdt-console-dot.yellow { background: #febc2e; }
  .vdt-console-dot.green { background: #28c840; }
  .vdt-console-body {
    background: #1f1720;
    color: #f8fafc;
    padding: 1rem 1.1rem;
    font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, "Liberation Mono", monospace;
    font-size: 0.95rem;
    line-height: 1.7;
    overflow-x: auto;
  }
  .vdt-code-line {
    display: block;
    white-space: pre;
  }
  .vdt-code-comment { color: #94a3b8; }
  .vdt-code-fn { color: #86efac; }
  .vdt-code-str { color: #fde68a; }
  .vdt-code-kw { color: #c4b5fd; }
  .vdt-code-out { color: #67e8f9; }

  .vdt-feature-grid {
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }
  .vdt-feature {
    padding: 1.35rem;
    position: relative;
    overflow: hidden;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }
  .vdt-feature::before {
    content: "";
    position: absolute;
    inset: 0 0 auto 0;
    height: 5px;
    background: linear-gradient(90deg, var(--vdt-primary), var(--vdt-primary-2));
  }
  .vdt-feature:hover {
    transform: translateY(-3px);
    box-shadow: 0 14px 30px rgba(120, 90, 40, 0.12);
  }
  .vdt-feature-icon {
    width: 52px;
    height: 52px;
    border-radius: 14px;
    display: grid;
    place-items: center;
    background: linear-gradient(135deg, rgba(183,121,31,0.12), rgba(212,160,23,0.18));
    color: var(--vdt-primary);
    font-size: 1.3rem;
    margin-bottom: 0.9rem;
  }
  .vdt-feature h3 {
    margin: 0 0 0.5rem;
    color: #3f2b12;
  }
  .vdt-feature p {
    margin: 0;
    color: var(--vdt-muted);
    line-height: 1.7;
  }

  .vdt-viz-shell {
    padding: 1.5rem;
  }
  .vdt-demo-note {
    margin: 0 0 1rem;
    padding: 0.9rem 1rem;
    border-radius: 14px;
    border: 1px solid #ead9af;
    background: #fff9e8;
    color: #6b5a27;
    line-height: 1.6;
  }
  .vdt-viz-layout {
    display: grid;
    grid-template-columns: minmax(0, 1.1fr) minmax(320px, 0.9fr);
    gap: 1.25rem;
    align-items: start;
  }
  .vdt-chart-card,
  .vdt-detail-card {
    padding: 1rem;
    border: 1px solid var(--vdt-border);
    border-radius: 18px;
    background: linear-gradient(180deg, #fff 0%, #fbf8f1 100%);
  }
  .vdt-toolbar {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    align-items: end;
    margin-bottom: 1rem;
  }
  .vdt-field {
    display: flex;
    flex-direction: column;
    gap: 0.35rem;
    min-width: 180px;
  }
  .vdt-field label {
    font-size: 0.85rem;
    font-weight: 700;
    color: var(--vdt-muted);
  }
  .vdt-field input[type="date"] {
    min-height: 44px;
    border: 1px solid var(--vdt-border);
    background: #fff;
    border-radius: 12px;
    padding: 0.7rem 0.85rem;
    color: var(--vdt-text);
    font: inherit;
  }
  .vdt-toggle-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.55rem;
    margin: 0.8rem 0 1rem;
  }
  .vdt-toggle {
    border: 1px solid var(--vdt-border);
    background: #fff;
    color: var(--vdt-text);
    border-radius: 999px;
    padding: 0.55rem 0.85rem;
    font: inherit;
    font-weight: 600;
    cursor: pointer;
  }
  .vdt-toggle.is-active {
    background: linear-gradient(135deg, var(--vdt-primary), var(--vdt-primary-2));
    color: #fff;
    border-color: transparent;
  }

  .vdt-svg-wrap {
    width: 100%;
    overflow: hidden;
    display: grid;
    place-items: center;
    padding: 0.5rem 0;
  }
  .vdt-legend {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 0.75rem;
    margin-top: 1rem;
  }
  .vdt-legend-item {
    display: flex;
    align-items: center;
    gap: 0.65rem;
    padding: 0.7rem 0.8rem;
    border-radius: 12px;
    background: #fff;
    border: 1px solid var(--vdt-border);
    font-size: 0.95rem;
  }
  .vdt-swatch {
    width: 14px;
    height: 14px;
    border-radius: 50%;
    flex: 0 0 14px;
  }

  .vdt-detail-card h3 {
    margin: 0 0 0.8rem;
    color: #3f2b12;
  }
  .vdt-date-pill {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.45rem 0.75rem;
    border-radius: 999px;
    background: rgba(183,121,31,0.08);
    color: var(--vdt-accent);
    font-weight: 700;
    margin-bottom: 1rem;
  }
  .vdt-detail-list {
    display: grid;
    gap: 0.75rem;
  }
  .vdt-detail-item {
    display: grid;
    grid-template-columns: 44px 1fr;
    gap: 0.85rem;
    align-items: start;
    padding: 0.9rem;
    border-radius: 16px;
    background: #fff;
    border: 1px solid var(--vdt-border);
  }
  .vdt-detail-icon {
    width: 44px;
    height: 44px;
    border-radius: 12px;
    display: grid;
    place-items: center;
    font-size: 1.1rem;
    color: var(--vdt-primary);
    background: linear-gradient(135deg, rgba(183,121,31,0.12), rgba(212,160,23,0.18));
  }
  .vdt-detail-item strong {
    display: block;
    margin-bottom: 0.2rem;
    color: #3f2b12;
  }
  .vdt-detail-item span,
  .vdt-detail-item small {
    display: block;
    color: var(--vdt-muted);
    line-height: 1.55;
  }

  .vdt-citation-card,
  .vdt-link-card {
    padding: 1.15rem;
  }
  .vdt-citation-card {
    border-left: 5px solid var(--vdt-primary);
  }
  .vdt-citation-card h3,
  .vdt-link-card h3 {
    margin-top: 0;
    color: #3f2b12;
  }
  .vdt-link-card a {
    color: var(--vdt-primary);
    text-decoration: none;
    font-weight: 700;
  }
  .vdt-link-card a:hover {
    text-decoration: underline;
  }
  .vdt-footer-note {
    margin-top: 2rem;
    color: var(--vdt-muted);
    font-size: 0.95rem;
    text-align: center;
  }
  .vdt-tooltip {
    position: fixed;
    z-index: 9999;
    pointer-events: none;
    background: #2a2116;
    color: #fff;
    border-radius: 12px;
    padding: 0.65rem 0.8rem;
    font-size: 0.85rem;
    line-height: 1.45;
    box-shadow: 0 16px 30px rgba(0,0,0,0.16);
    opacity: 0;
    transform: translateY(4px);
    transition: opacity 0.15s ease, transform 0.15s ease;
    max-width: 240px;
  }
  .vdt-tooltip.is-visible {
    opacity: 1;
    transform: translateY(0);
  }

  @media (max-width: 960px) {
    .vdt-hero-grid,
    .vdt-viz-layout,
    .vdt-feature-grid,
    .vdt-meta-grid,
    .vdt-stat-grid,
    .vdt-links-grid {
      grid-template-columns: 1fr;
    }
    .vdt-logo {
      max-width: 120px;
    }
  }
</style>

<div class="vdt-page">
  <div class="vdt-wrap">
    <section class="vdt-card vdt-hero">
      <div class="vdt-hero-grid">
        <div class="vdt-logo-box">
          <img
            src="/assets/vedicdatetime/VedicDateTimeLogo%20(2).png"
            alt="VedicDateTime logo"
            class="vdt-logo"
          >
        </div>
        <div>
          <span class="vdt-kicker">R package showcase</span>
          <h1 class="vdt-title">VedicDateTime</h1>
          <p class="vdt-subtitle">
            VedicDateTime: Vedic Calendar System. Provides platform for Vedic calendar system having several functionalities to facilitate conversion between Gregorian and Vedic calendar systems, and helpful in examining its impact in the time series analysis domain.
          </p>
          <div class="vdt-actions">
            <a class="vdt-btn vdt-btn-primary" href="https://CRAN.R-project.org/package=VedicDateTime" target="_blank" rel="noopener">View on CRAN</a>
            <a class="vdt-btn vdt-btn-secondary" href="https://github.com/neerajdhanraj/VedicDateTime" target="_blank" rel="noopener">GitHub repository</a>
            <a class="vdt-btn vdt-btn-secondary" href="https://doi.org/10.1007/s11042-023-16553-w" target="_blank" rel="noopener">Read the article</a>
          </div>
        </div>
      </div>

      <div class="vdt-stat-grid">
        <div class="vdt-stat"><strong>0.1.9</strong><span>Current CRAN version</span></div>
        <div class="vdt-stat"><strong>5</strong><span>Panchanga elements</span></div>
        <div class="vdt-stat"><strong>27</strong><span>Nakshatras supported</span></div>
        <div class="vdt-stat"><strong>GPL 3</strong><span>Open source license</span></div>
      </div>
    </section>

    <section class="vdt-section">
      <div class="vdt-card vdt-overview">
        <div class="vdt-section-head">
          <h2>Package overview</h2>
          <p>
            VedicDateTime implements the Vedic calendar system in R and supports conversion between Gregorian and Vedic calendar systems. It is useful for Panchanga calculations and for studying calendar effects in time series analysis.
          </p>
        </div>

        <div class="vdt-meta-grid">
          <div class="vdt-meta-item">
            <span class="label">Authors</span>
            <div class="value">Neeraj Dhanraj Bokde, Prajwal Kailasnath Patil, Saradindu Sengupta, Andrés Elías Feijóo Lorenzo</div>
          </div>
          <div class="vdt-meta-item">
            <span class="label">Maintainer</span>
            <div class="value">Neeraj Dhanraj Bokde &lt;neerajdhanraj at gmail.com&gt;</div>
          </div>
          <div class="vdt-meta-item">
            <span class="label">Published on CRAN</span>
            <div class="value">2023 09 20</div>
          </div>
          <div class="vdt-meta-item">
            <span class="label">License</span>
            <div class="value">GPL (≥ 3)</div>
          </div>
          <div class="vdt-meta-item">
            <span class="label">Depends</span>
            <div class="value">R (≥ 3.1.0)</div>
          </div>
          <div class="vdt-meta-item">
            <span class="label">DOI</span>
            <div class="value">10.32614/CRAN.package.VedicDateTime</div>
          </div>
        </div>

        <div class="vdt-console" aria-label="R console example">
          <div class="vdt-console-bar">
            <span class="vdt-console-dot red"></span>
            <span class="vdt-console-dot yellow"></span>
            <span class="vdt-console-dot green"></span>
          </div>
          <div class="vdt-console-body">
            <span class="vdt-code-line"><span class="vdt-code-comment"># Install from CRAN</span></span>
            <span class="vdt-code-line"><span class="vdt-code-fn">install.packages</span>(<span class="vdt-code-str">"VedicDateTime"</span>)</span>
            <span class="vdt-code-line"> </span>
            <span class="vdt-code-line"><span class="vdt-code-comment"># Load the package</span></span>
            <span class="vdt-code-line"><span class="vdt-code-fn">library</span>(VedicDateTime)</span>
            <span class="vdt-code-line"> </span>
            <span class="vdt-code-line"><span class="vdt-code-comment"># Get Panchanga elements for a date</span></span>
            <span class="vdt-code-line">date <span class="vdt-code-kw">&lt;-</span> <span class="vdt-code-fn">as.Date</span>(<span class="vdt-code-str">"2024-01-15"</span>)</span>
            <span class="vdt-code-line"><span class="vdt-code-fn">tithi</span>(date)</span>
            <span class="vdt-code-line"><span class="vdt-code-out">#&gt; [1] "Panchami"</span></span>
            <span class="vdt-code-line"><span class="vdt-code-fn">nakshatra</span>(date)</span>
            <span class="vdt-code-line"><span class="vdt-code-out">#&gt; [1] "Rohini"</span></span>
            <span class="vdt-code-line"><span class="vdt-code-fn">vaara</span>(date)</span>
            <span class="vdt-code-line"><span class="vdt-code-out">#&gt; [1] "Somvar"</span></span>
            <span class="vdt-code-line"><span class="vdt-code-fn">yoga</span>(date)</span>
            <span class="vdt-code-line"><span class="vdt-code-out">#&gt; [1] "Saubhagya"</span></span>
            <span class="vdt-code-line"><span class="vdt-code-fn">karana</span>(date)</span>
            <span class="vdt-code-line"><span class="vdt-code-out">#&gt; [1] "Taitila"</span></span>
          </div>
        </div>
      </div>
    </section>

    <section class="vdt-section">
      <div class="vdt-section-head">
        <h2>Core Panchanga features</h2>
        <p>
          The package supports the major components of the Vedic calendar and exposes them in a way that is practical for computation, exploration, and research workflows.
        </p>
      </div>
      <div class="vdt-feature-grid">
        <article class="vdt-card vdt-feature">
          <div class="vdt-feature-icon">☉</div>
          <h3>Vaara</h3>
          <p>Compute the weekday in the Vedic calendar context and use it as a simple but meaningful calendar feature.</p>
        </article>
        <article class="vdt-card vdt-feature">
          <div class="vdt-feature-icon">☽</div>
          <h3>Tithi</h3>
          <p>Work with lunar days that shape many Panchanga based analyses and observances.</p>
        </article>
        <article class="vdt-card vdt-feature">
          <div class="vdt-feature-icon">★</div>
          <h3>Nakshatra</h3>
          <p>Track the lunar mansion and incorporate one of the most recognizable Vedic calendar dimensions.</p>
        </article>
        <article class="vdt-card vdt-feature">
          <div class="vdt-feature-icon">✦</div>
          <h3>Yoga</h3>
          <p>Explore yoga values that enrich Panchanga interpretation and provide another cyclic astronomical layer.</p>
        </article>
        <article class="vdt-card vdt-feature">
          <div class="vdt-feature-icon">◐</div>
          <h3>Karana</h3>
          <p>Use half tithi units for finer granularity in day level Vedic calendar interpretation.</p>
        </article>
        <article class="vdt-card vdt-feature">
          <div class="vdt-feature-icon">⌘</div>
          <h3>Calendar conversion</h3>
          <p>Bridge Gregorian and Vedic calendar systems for research, interpretation, and time series feature engineering.</p>
        </article>
      </div>
    </section>

    <section class="vdt-section">
      <div class="vdt-card vdt-viz-shell">
        <div class="vdt-section-head">
          <h2>Panchanga visualization</h2>
          <p>
            This interactive view illustrates how VedicDateTime style outputs can be explored on the web. It uses documentation grounded demo data for display. Connect real package output later for production use.
          </p>
        </div>

        <p class="vdt-demo-note">
          Demo mode. The chart below is driven by deterministic illustrative values derived from the selected date so that the interaction works for any day. Replace the demo generator with real VedicDateTime output if you want production accurate Panchanga results.
        </p>

        <div class="vdt-viz-layout">
          <div class="vdt-chart-card">
            <div class="vdt-toolbar">
              <div class="vdt-field">
                <label for="vdt-date">Select a date</label>
                <input id="vdt-date" type="date" value="2024-01-15">
              </div>
              <button class="vdt-btn vdt-btn-secondary" id="vdt-today" type="button">Today</button>
            </div>

            <div class="vdt-toggle-row" id="vdt-toggles"></div>

            <div class="vdt-svg-wrap">
              <svg id="vdt-chart" viewBox="0 0 680 680" width="100%" style="max-width:640px;height:auto;" aria-label="Panchanga radial chart"></svg>
            </div>

            <div class="vdt-legend">
              <div class="vdt-legend-item"><span class="vdt-swatch" style="background:#c0841a;"></span>Vaara ring</div>
              <div class="vdt-legend-item"><span class="vdt-swatch" style="background:#d4a017;"></span>Tithi ring</div>
              <div class="vdt-legend-item"><span class="vdt-swatch" style="background:#6aa84f;"></span>Nakshatra ring</div>
              <div class="vdt-legend-item"><span class="vdt-swatch" style="background:#0f766e;"></span>Yoga ring</div>
              <div class="vdt-legend-item"><span class="vdt-swatch" style="background:#8b5cf6;"></span>Karana ring</div>
              <div class="vdt-legend-item"><span class="vdt-swatch" style="background:#f59e0b;"></span>Center summary</div>
            </div>
          </div>

          <aside class="vdt-detail-card">
            <div class="vdt-date-pill" id="vdt-date-pill">Selected date</div>
            <h3>Selected Panchanga details</h3>
            <div class="vdt-detail-list" id="vdt-details"></div>
          </aside>
        </div>
      </div>
    </section>

    <section class="vdt-section">
      <div class="vdt-section-head">
        <h2>Publication and citation</h2>
        <p>
          Use the following article when citing the methodological and package work in publications or presentations.
        </p>
      </div>
      <div class="vdt-card vdt-citation-card">
        <h3>Article citation</h3>
        <p>
          Bokde, Neeraj Dhanraj, Patil, Prajwal Kailasnath, Sengupta, Saradindu, Sawant, Manisha, and Feijóo-Lorenzo, Andrés E. 2024. VedicDateTime: An R package to implement Vedic calendar system. <em>Multimedia Tools and Applications</em>, 83(11), 32141 to 32157.
        </p>
        <p>
          DOI:
          <a href="https://doi.org/10.1007/s11042-023-16553-w" target="_blank" rel="noopener">https://doi.org/10.1007/s11042-023-16553-w</a>
        </p>
        <pre style="white-space:pre-wrap;background:#faf7ef;border:1px solid var(--vdt-border);padding:1rem;border-radius:14px;overflow:auto;">@article{bokde2024vedicdatetime,
  title={VedicDateTime: An R package to implement Vedic calendar system},
  author={Bokde, Neeraj Dhanraj and Patil, Prajwal Kailasnath and Sengupta, Saradindu and Sawant, Manisha and Feij{\'o}o-Lorenzo, Andr{\'e}s E},
  journal={Multimedia Tools and Applications},
  volume={83},
  number={11},
  pages={32141--32157},
  year={2024},
  publisher={Springer}
}</pre>
      </div>
    </section>

    <section class="vdt-section">
      <div class="vdt-section-head">
        <h2>Links and resources</h2>
        <p>
          Direct resources for package access, documentation, issue tracking, and article discovery.
        </p>
      </div>
      <div class="vdt-links-grid" style="grid-template-columns:repeat(2,minmax(0,1fr));">
        <div class="vdt-card vdt-link-card">
          <h3>CRAN package page</h3>
          <p><a href="https://CRAN.R-project.org/package=VedicDateTime" target="_blank" rel="noopener">https://CRAN.R-project.org/package=VedicDateTime</a></p>
        </div>
        <div class="vdt-card vdt-link-card">
          <h3>GitHub repository</h3>
          <p><a href="https://github.com/neerajdhanraj/VedicDateTime" target="_blank" rel="noopener">https://github.com/neerajdhanraj/VedicDateTime</a></p>
        </div>
        <div class="vdt-card vdt-link-card">
          <h3>Package website</h3>
          <p><a href="https://www.neerajbokde.in/viggnette/2022-09-05-VedicDateTime" target="_blank" rel="noopener">https://www.neerajbokde.in/viggnette/2022-09-05-VedicDateTime</a></p>
        </div>
        <div class="vdt-card vdt-link-card">
          <h3>Bug reports</h3>
          <p><a href="https://github.com/prajwalkpatil/VedicDateTime/issues" target="_blank" rel="noopener">https://github.com/prajwalkpatil/VedicDateTime/issues</a></p>
        </div>
      </div>
    </section>

    <p class="vdt-footer-note">
      This page is designed for direct inclusion in a Jekyll website. The interactive visualization is a website demo based on documented VedicDateTime concepts and should be connected to actual package outputs for analytical use.
    </p>
  </div>
</div>

<div class="vdt-tooltip" id="vdt-tooltip"></div>

<script>
(function () {
  const WEEKDAYS = [
    { name: "Ravivar", english: "Sunday", deity: "Surya" },
    { name: "Somvar", english: "Monday", deity: "Chandra" },
    { name: "Mangalvar", english: "Tuesday", deity: "Mangala" },
    { name: "Budhvar", english: "Wednesday", deity: "Budha" },
    { name: "Guruvar", english: "Thursday", deity: "Brihaspati" },
    { name: "Shukravar", english: "Friday", deity: "Shukra" },
    { name: "Shanivar", english: "Saturday", deity: "Shani" }
  ];

  const TITHIS = [
    "Pratipada","Dvitiya","Tritiya","Chaturthi","Panchami","Shashthi","Saptami","Ashtami","Navami","Dashami",
    "Ekadashi","Dwadashi","Trayodashi","Chaturdashi","Purnima","Pratipada Krishna","Dvitiya Krishna",
    "Tritiya Krishna","Chaturthi Krishna","Panchami Krishna","Shashthi Krishna","Saptami Krishna",
    "Ashtami Krishna","Navami Krishna","Dashami Krishna","Ekadashi Krishna","Dwadashi Krishna",
    "Trayodashi Krishna","Chaturdashi Krishna","Amavasya"
  ];

  const NAKSHATRAS = [
    "Ashwini","Bharani","Krittika","Rohini","Mrigashira","Ardra","Punarvasu","Pushya","Ashlesha","Magha",
    "Purva Phalguni","Uttara Phalguni","Hasta","Chitra","Swati","Vishakha","Anuradha","Jyeshtha","Mula",
    "Purva Ashadha","Uttara Ashadha","Shravana","Dhanishta","Shatabhisha","Purva Bhadrapada",
    "Uttara Bhadrapada","Revati"
  ];

  const YOGAS = [
    "Vishkumbha","Priti","Ayushman","Saubhagya","Shobhana","Atiganda","Sukarman","Dhriti","Shula","Ganda",
    "Vriddhi","Dhruva","Vyaghata","Harshana","Vajra","Siddhi","Vyatipata","Variyana","Parigha","Shiva",
    "Siddha","Sadhya","Shubha","Shukla","Brahma","Indra","Vaidhriti"
  ];

  const KARANAS = [
    "Bava","Balava","Kaulava","Taitila","Garaja","Vanija","Vishti","Shakuni","Chatushpada","Naga","Kimstughna"
  ];

  const COLORS = {
    vaara: "#c0841a",
    tithi: "#d4a017",
    nakshatra: "#6aa84f",
    yoga: "#0f766e",
    karana: "#8b5cf6"
  };

  const visibleRings = {
    vaara: true,
    tithi: true,
    nakshatra: true,
    yoga: true,
    karana: true
  };

  const dateInput = document.getElementById("vdt-date");
  const todayBtn = document.getElementById("vdt-today");
  const detailsEl = document.getElementById("vdt-details");
  const chartEl = document.getElementById("vdt-chart");
  const togglesEl = document.getElementById("vdt-toggles");
  const datePillEl = document.getElementById("vdt-date-pill");
  const tooltipEl = document.getElementById("vdt-tooltip");

  function pad(n) {
    return String(n).padStart(2, "0");
  }

  function formatHumanDate(dateObj) {
    return dateObj.toLocaleDateString(undefined, {
      weekday: "long",
      year: "numeric",
      month: "long",
      day: "numeric"
    });
  }

  function endTimeFromSeed(seed, offset) {
    const total = 20 * 60 + ((seed * 37 + offset * 71) % (13 * 60));
    const h = Math.floor(total / 60);
    const m = total % 60;
    return h + ":" + pad(m);
  }

  function getDaySeed(dateStr) {
    const d = new Date(dateStr + "T00:00:00");
    return Math.floor(d.getTime() / 86400000);
  }

  function generatePanchangaForDate(dateStr) {
    const seed = getDaySeed(dateStr);
    const jsDate = new Date(dateStr + "T00:00:00");
    const weekday = WEEKDAYS[jsDate.getDay()];
    const tithiIndex = Math.abs(seed * 3 + 4) % TITHIS.length;
    const nakshatraIndex = Math.abs(seed * 5 + 7) % NAKSHATRAS.length;
    const yogaIndex = Math.abs(seed * 7 + 3) % YOGAS.length;
    const karanaIndex = Math.abs(seed * 11 + 2) % KARANAS.length;

    return {
      date: dateStr,
      formattedDate: formatHumanDate(jsDate),
      vaara: {
        icon: "☉",
        label: "Vaara",
        name: weekday.name,
        sub: weekday.english,
        extra: "Deity: " + weekday.deity,
        end: "Full day"
      },
      tithi: {
        icon: "☽",
        label: "Tithi",
        name: TITHIS[tithiIndex],
        sub: "Lunar day",
        extra: "Ends at " + endTimeFromSeed(seed, 1),
        end: endTimeFromSeed(seed, 1)
      },
      nakshatra: {
        icon: "★",
        label: "Nakshatra",
        name: NAKSHATRAS[nakshatraIndex],
        sub: "Lunar mansion",
        extra: "Ends at " + endTimeFromSeed(seed, 2),
        end: endTimeFromSeed(seed, 2)
      },
      yoga: {
        icon: "✦",
        label: "Yoga",
        name: YOGAS[yogaIndex],
        sub: "Astronomical combination",
        extra: "Ends at " + endTimeFromSeed(seed, 3),
        end: endTimeFromSeed(seed, 3)
      },
      karana: {
        icon: "◐",
        label: "Karana",
        name: KARANAS[karanaIndex],
        sub: "Half tithi",
        extra: "Ends at " + endTimeFromSeed(seed, 4),
        end: endTimeFromSeed(seed, 4)
      }
    };
  }

  function polarToCartesian(cx, cy, r, angleDeg) {
    const a = (angleDeg - 90) * Math.PI / 180;
    return { x: cx + r * Math.cos(a), y: cy + r * Math.sin(a) };
  }

  function donutPath(cx, cy, rOuter, rInner, startAngle, endAngle) {
    const p1 = polarToCartesian(cx, cy, rOuter, endAngle);
    const p2 = polarToCartesian(cx, cy, rOuter, startAngle);
    const p3 = polarToCartesian(cx, cy, rInner, startAngle);
    const p4 = polarToCartesian(cx, cy, rInner, endAngle);
    const largeArc = endAngle - startAngle <= 180 ? "0" : "1";
    return [
      "M", p1.x, p1.y,
      "A", rOuter, rOuter, 0, largeArc, 0, p2.x, p2.y,
      "L", p3.x, p3.y,
      "A", rInner, rInner, 0, largeArc, 1, p4.x, p4.y,
      "Z"
    ].join(" ");
  }

  function renderDetails(data) {
    datePillEl.textContent = data.formattedDate;
    const items = ["vaara", "tithi", "nakshatra", "yoga", "karana"].map((key) => {
      const item = data[key];
      return `
        <div class="vdt-detail-item">
          <div class="vdt-detail-icon">${item.icon}</div>
          <div>
            <strong>${item.label}: ${item.name}</strong>
            <span>${item.sub}</span>
            <small>${item.extra}</small>
          </div>
        </div>
      `;
    }).join("");
    detailsEl.innerHTML = items;
  }

  function showTooltip(html, x, y) {
    tooltipEl.innerHTML = html;
    tooltipEl.style.left = (x + 14) + "px";
    tooltipEl.style.top = (y + 14) + "px";
    tooltipEl.classList.add("is-visible");
  }

  function hideTooltip() {
    tooltipEl.classList.remove("is-visible");
  }

  function attachTooltip(node, html) {
    node.addEventListener("mousemove", (e) => showTooltip(html, e.clientX, e.clientY));
    node.addEventListener("mouseleave", hideTooltip);
    node.addEventListener("blur", hideTooltip);
  }

  function renderChart(data) {
    const cx = 340;
    const cy = 340;
    const defs = `
      <defs>
        <filter id="vdtShadow" x="-20%" y="-20%" width="140%" height="140%">
          <feDropShadow dx="0" dy="8" stdDeviation="8" flood-color="rgba(120,90,40,0.18)"/>
        </filter>
      </defs>
    `;

    const rings = [
      { key: "vaara", inner: 92, outer: 138, start: 0, end: 360, text: data.vaara.name },
      { key: "tithi", inner: 146, outer: 198, start: 12, end: 348, text: data.tithi.name },
      { key: "nakshatra", inner: 206, outer: 258, start: 24, end: 336, text: data.nakshatra.name },
      { key: "yoga", inner: 266, outer: 318, start: 36, end: 324, text: data.yoga.name },
      { key: "karana", inner: 326, outer: 372, start: 48, end: 312, text: data.karana.name }
    ];

    const ringSvg = rings.map((ring) => {
      if (!visibleRings[ring.key]) return "";
      const path = donutPath(cx, cy, ring.outer, ring.inner, ring.start, ring.end);
      const midAngle = (ring.start + ring.end) / 2;
      const textPos = polarToCartesian(cx, cy, (ring.inner + ring.outer) / 2, midAngle);
      return `
        <path
          d="${path}"
          fill="${COLORS[ring.key]}"
          fill-opacity="0.9"
          stroke="#fffaf0"
          stroke-width="3"
          filter="url(#vdtShadow)"
          data-key="${ring.key}"
          tabindex="0"
        ></path>
        <text x="${textPos.x}" y="${textPos.y}" text-anchor="middle" dominant-baseline="middle"
          font-size="15" font-weight="700" fill="#fff">${ring.text}</text>
      `;
    }).join("");

    const center = `
      <circle cx="${cx}" cy="${cy}" r="78" fill="#fff9ec" stroke="#ead9af" stroke-width="3"></circle>
      <text x="${cx}" y="${cy - 18}" text-anchor="middle" font-size="18" font-weight="700" fill="#6f4a16">Panchanga</text>
      <text x="${cx}" y="${cy + 10}" text-anchor="middle" font-size="15" fill="#6b7280">${data.vaara.name}</text>
      <text x="${cx}" y="${cy + 34}" text-anchor="middle" font-size="13" fill="#8b5e34">${data.tithi.name}</text>
    `;

    chartEl.innerHTML = defs + ringSvg + center;

    chartEl.querySelectorAll("path[data-key]").forEach((node) => {
      const key = node.getAttribute("data-key");
      const item = data[key];
      attachTooltip(node, `<strong>${item.label}</strong><br>${item.name}<br><span>${item.extra}</span>`);
    });
  }

  function renderToggles() {
    const labels = {
      vaara: "Vaara",
      tithi: "Tithi",
      nakshatra: "Nakshatra",
      yoga: "Yoga",
      karana: "Karana"
    };
    togglesEl.innerHTML = Object.keys(labels).map((key) => `
      <button type="button" class="vdt-toggle ${visibleRings[key] ? 'is-active' : ''}" data-key="${key}">
        ${labels[key]}
      </button>
    `).join("");

    togglesEl.querySelectorAll(".vdt-toggle").forEach((btn) => {
      btn.addEventListener("click", () => {
        const key = btn.getAttribute("data-key");
        visibleRings[key] = !visibleRings[key];
        btn.classList.toggle("is-active", visibleRings[key]);
        updateView();
      });
    });
  }

  function updateView() {
    const data = generatePanchangaForDate(dateInput.value);
    renderDetails(data);
    renderChart(data);
  }

  function todayIso() {
    const now = new Date();
    return now.getFullYear() + "-" + pad(now.getMonth() + 1) + "-" + pad(now.getDate());
  }

  todayBtn.addEventListener("click", () => {
    dateInput.value = todayIso();
    updateView();
  });

  dateInput.addEventListener("change", updateView);

  renderToggles();
  if (!dateInput.value) dateInput.value = "2024-01-15";
  updateView();
})();
</script>
