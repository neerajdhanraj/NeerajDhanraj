---
layout: default
title: VedicDateTime
permalink: /vedicdatetime/
---

<style>
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

:root {
    --vdt-primary: #b8860b;
    --vdt-primary-light: #daa520;
    --vdt-primary-dark: #8b6914;
    --vdt-primary-bg: rgba(184, 134, 11, 0.08);
    --vdt-accent: #d2691e;
    --vdt-bg: #ffffff;
    --vdt-bg-alt: #fafbfc;
    --vdt-bg-warm: #fffcf5;
    --vdt-bg-code: #1e1e2e;
    --vdt-border: #e5e7eb;
    --vdt-border-light: #f0f0f0;
    --vdt-text: #1f2937;
    --vdt-text-secondary: #4b5563;
    --vdt-text-muted: #6b7280;
    --vdt-text-light: #9ca3af;
    --vdt-success: #059669;
    --vdt-info: #2563eb;
    --vdt-vaara: #dc2626;
    --vdt-tithi: #0891b2;
    --vdt-nakshatra: #d97706;
    --vdt-yoga: #059669;
    --vdt-karana: #ea580c;
    --vdt-space-xs: 4px;
    --vdt-space-sm: 8px;
    --vdt-space-md: 16px;
    --vdt-space-lg: 24px;
    --vdt-space-xl: 48px;
    --vdt-space-2xl: 72px;
    --vdt-font: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
    --vdt-font-mono: "SF Mono", "Fira Code", "Fira Mono", Consolas, "Liberation Mono", Menlo, monospace;
    --vdt-max-width: 1140px;
    --vdt-radius-sm: 6px;
    --vdt-radius: 10px;
    --vdt-radius-lg: 16px;
    --vdt-shadow-sm: 0 1px 2px rgba(0,0,0,0.04);
    --vdt-shadow: 0 4px 6px -1px rgba(0,0,0,0.07), 0 2px 4px -1px rgba(0,0,0,0.04);
    --vdt-shadow-lg: 0 10px 25px -5px rgba(0,0,0,0.08), 0 8px 10px -6px rgba(0,0,0,0.03);
    --vdt-shadow-xl: 0 20px 40px -10px rgba(0,0,0,0.1);
}

.vdt-showcase {
    font-family: var(--vdt-font);
    background: var(--vdt-bg);
    color: var(--vdt-text);
    line-height: 1.65;
    font-size: 16px;
    -webkit-font-smoothing: antialiased;
}
.vdt-container {
    max-width: var(--vdt-max-width);
    margin: 0 auto;
    padding: 0 var(--vdt-space-lg);
}
.vdt-section {
    padding: var(--vdt-space-2xl) 0;
}
.vdt-showcase h1, .vdt-showcase h2, .vdt-showcase h3, .vdt-showcase h4 {
    font-weight: 700;
    line-height: 1.25;
    color: var(--vdt-text);
    letter-spacing: -0.02em;
}
.vdt-showcase h1 { font-size: 2.5rem; margin-bottom: var(--vdt-space-md); }
.vdt-showcase h2 { font-size: 1.875rem; margin-bottom: var(--vdt-space-lg); }
.vdt-showcase h3 { font-size: 1.25rem; margin-bottom: var(--vdt-space-sm); }
.vdt-showcase p { margin-bottom: var(--vdt-space-md); color: var(--vdt-text-secondary); }
.vdt-showcase a { color: var(--vdt-info); text-decoration: none; transition: color 0.15s ease; }
.vdt-showcase a:hover { color: var(--vdt-primary-dark); text-decoration: underline; }
.vdt-label {
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    color: var(--vdt-primary);
}
.vdt-badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    background: var(--vdt-primary-bg);
    border: 1px solid var(--vdt-primary-light);
    border-radius: 50px;
    font-size: 0.8rem;
    font-weight: 600;
    color: var(--vdt-primary-dark);
}
.vdt-btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 12px 24px;
    border: 1px solid var(--vdt-border);
    border-radius: var(--vdt-radius);
    background: var(--vdt-bg);
    color: var(--vdt-text);
    font-size: 0.95rem;
    font-weight: 600;
    text-decoration: none;
    cursor: pointer;
    transition: all 0.2s ease;
    box-shadow: var(--vdt-shadow-sm);
}
.vdt-btn:hover { 
    background: var(--vdt-bg-alt); 
    border-color: var(--vdt-primary-light);
    text-decoration: none;
    box-shadow: var(--vdt-shadow);
    transform: translateY(-1px);
}
.vdt-btn-primary {
    background: linear-gradient(135deg, var(--vdt-primary-light) 0%, var(--vdt-primary) 100%);
    border: none;
    color: white;
    box-shadow: 0 4px 14px rgba(184, 134, 11, 0.25);
}
.vdt-btn-primary:hover { 
    background: linear-gradient(135deg, var(--vdt-primary) 0%, var(--vdt-primary-dark) 100%);
    box-shadow: 0 6px 20px rgba(184, 134, 11, 0.35);
}
.vdt-btn svg { width: 18px; height: 18px; }
.vdt-card {
    background: var(--vdt-bg);
    border: 1px solid var(--vdt-border);
    border-radius: var(--vdt-radius-lg);
    padding: var(--vdt-space-lg);
    box-shadow: var(--vdt-shadow);
    transition: all 0.25s ease;
}
.vdt-card:hover {
    box-shadow: var(--vdt-shadow-lg);
    border-color: var(--vdt-border-light);
}
.vdt-divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--vdt-border), transparent);
    margin: var(--vdt-space-xl) 0;
}
.vdt-section-header {
    text-align: center;
    max-width: 640px;
    margin: 0 auto var(--vdt-space-xl);
}
.vdt-section-header .vdt-label {
    margin-bottom: var(--vdt-space-sm);
    display: block;
}
.vdt-section-header p {
    font-size: 1.1rem;
    color: var(--vdt-text-muted);
    margin-bottom: 0;
}
.vdt-header {
    padding: var(--vdt-space-2xl) 0;
    text-align: center;
    background: linear-gradient(180deg, var(--vdt-bg-warm) 0%, var(--vdt-bg) 100%);
    border-bottom: 1px solid var(--vdt-border);
    position: relative;
    overflow: hidden;
}
.vdt-header::before {
    content: "";
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 100%;
    max-width: 800px;
    height: 100%;
    background: radial-gradient(ellipse at 50% 0%, var(--vdt-primary-bg) 0%, transparent 70%);
    pointer-events: none;
}
.vdt-header > * { position: relative; }
.vdt-header-logo { margin-bottom: var(--vdt-space-lg); }
.vdt-logo {
    max-width: 180px;
    height: auto;
    display: block;
    margin: 0 auto;
    border-radius: var(--vdt-radius);
}
.vdt-header-badge { margin-bottom: var(--vdt-space-md); }
.vdt-header h1 { 
    color: var(--vdt-text);
    font-size: 3rem;
    letter-spacing: -0.03em;
}
.vdt-header-tagline {
    font-size: 1.25rem;
    color: var(--vdt-text-secondary);
    max-width: 580px;
    margin: 0 auto var(--vdt-space-lg);
    line-height: 1.5;
}
.vdt-header-actions {
    display: flex;
    justify-content: center;
    gap: var(--vdt-space-md);
    flex-wrap: wrap;
    margin-bottom: var(--vdt-space-xl);
}
.vdt-header-meta {
    display: flex;
    justify-content: center;
    gap: var(--vdt-space-xl);
    flex-wrap: wrap;
    padding-top: var(--vdt-space-lg);
    border-top: 1px solid var(--vdt-border);
}
.vdt-meta-item { text-align: center; }
.vdt-meta-item .value {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--vdt-primary);
}
.vdt-meta-item .label {
    font-size: 0.8rem;
    color: var(--vdt-text-muted);
    text-transform: uppercase;
    letter-spacing: 0.05em;
}
.vdt-overview { background: var(--vdt-bg); }
.vdt-overview-grid {
    display: grid;
    grid-template-columns: 1fr 1.1fr;
    gap: var(--vdt-space-xl);
    align-items: start;
}
@media (max-width: 900px) {
    .vdt-overview-grid { grid-template-columns: 1fr; }
}
.vdt-overview-content h2 { font-size: 1.75rem; }
.vdt-overview-content p { font-size: 1.05rem; line-height: 1.75; }
.vdt-pkg-meta {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: var(--vdt-space-md);
    margin-top: var(--vdt-space-lg);
    padding-top: var(--vdt-space-lg);
    border-top: 1px solid var(--vdt-border);
}
.vdt-pkg-meta-item { display: flex; flex-direction: column; gap: 2px; }
.vdt-pkg-meta-item .label {
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.03em;
    color: var(--vdt-text-muted);
}
.vdt-pkg-meta-item .value {
    font-size: 0.95rem;
    color: var(--vdt-text);
    font-weight: 500;
}
.vdt-pkg-meta-item .value a { color: var(--vdt-info); }
.vdt-code-block {
    background: var(--vdt-bg-code);
    border-radius: var(--vdt-radius-lg);
    overflow: hidden;
    box-shadow: var(--vdt-shadow-xl);
}
.vdt-code-header {
    display: flex;
    align-items: center;
    gap: var(--vdt-space-sm);
    padding: 14px 20px;
    background: #262636;
    border-bottom: 1px solid #3a3a4a;
}
.vdt-code-dots { display: flex; gap: 8px; }
.vdt-code-dot { width: 12px; height: 12px; border-radius: 50%; }
.vdt-code-dot.red { background: #ff5f57; }
.vdt-code-dot.yellow { background: #febc2e; }
.vdt-code-dot.green { background: #28c840; }
.vdt-code-title {
    margin-left: auto;
    font-size: 0.8rem;
    color: #8b8b9a;
    font-weight: 500;
}
.vdt-code-body {
    padding: 24px;
    font-family: var(--vdt-font-mono);
    font-size: 0.9rem;
    line-height: 1.9;
    overflow-x: auto;
    color: #e4e4ef;
}
.vdt-code-body .code-line { min-height: 1.5em; }
.vdt-code-body .comment { color: #6a737d; font-style: italic; }
.vdt-code-body .keyword { color: #ff79c6; }
.vdt-code-body .function { color: #50fa7b; }
.vdt-code-body .string { color: #f1fa8c; }
.vdt-code-body .output { color: #8be9fd; }
.vdt-code-body .prompt { color: #bd93f9; }
.vdt-features {
    background: var(--vdt-bg-alt);
    border-top: 1px solid var(--vdt-border);
    border-bottom: 1px solid var(--vdt-border);
}
.vdt-features-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: var(--vdt-space-lg);
}
@media (max-width: 900px) {
    .vdt-features-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (max-width: 600px) {
    .vdt-features-grid { grid-template-columns: 1fr; }
}
.vdt-feature-card {
    background: var(--vdt-bg);
    border: 1px solid var(--vdt-border);
    border-radius: var(--vdt-radius-lg);
    padding: var(--vdt-space-lg) var(--vdt-space-lg) var(--vdt-space-xl);
    text-align: center;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
}
.vdt-feature-card::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--vdt-primary-light), var(--vdt-accent));
    opacity: 0;
    transition: opacity 0.3s ease;
}
.vdt-feature-card:hover {
    transform: translateY(-4px);
    box-shadow: var(--vdt-shadow-lg);
    border-color: var(--vdt-primary-light);
}
.vdt-feature-card:hover::before { opacity: 1; }
.vdt-feature-icon {
    width: 64px;
    height: 64px;
    margin: 0 auto var(--vdt-space-md);
    background: linear-gradient(135deg, var(--vdt-primary-bg), rgba(218, 165, 32, 0.15));
    border: 2px solid var(--vdt-primary-bg);
    border-radius: 16px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.75rem;
    transition: all 0.3s ease;
}
.vdt-feature-card:hover .vdt-feature-icon {
    transform: scale(1.1);
    border-color: var(--vdt-primary-light);
}
.vdt-feature-card h3 {
    color: var(--vdt-text);
    margin-bottom: var(--vdt-space-sm);
    font-size: 1.1rem;
}
.vdt-feature-card p {
    font-size: 0.9rem;
    color: var(--vdt-text-muted);
    margin-bottom: 0;
    line-height: 1.6;
}
.vdt-viz { background: var(--vdt-bg); }
.vdt-viz-container {
    border: 1px solid var(--vdt-border);
    border-radius: var(--vdt-radius-lg);
    overflow: hidden;
    background: var(--vdt-bg);
    box-shadow: var(--vdt-shadow);
}
.vdt-viz-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: var(--vdt-space-md) var(--vdt-space-lg);
    background: var(--vdt-bg-alt);
    border-bottom: 1px solid var(--vdt-border);
    flex-wrap: wrap;
    gap: var(--vdt-space-md);
}
.vdt-viz-title {
    font-weight: 600;
    display: flex;
    align-items: center;
    gap: 10px;
    color: var(--vdt-text);
}
.vdt-viz-title svg { width: 22px; height: 22px; color: var(--vdt-primary); }
.vdt-viz-controls { display: flex; gap: 8px; flex-wrap: wrap; }
.vdt-ring-btn {
    padding: 6px 14px;
    border: 2px solid;
    background: transparent;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s ease;
}
.vdt-ring-btn[data-ring="vaara"] { border-color: var(--vdt-vaara); color: var(--vdt-vaara); }
.vdt-ring-btn[data-ring="tithi"] { border-color: var(--vdt-tithi); color: var(--vdt-tithi); }
.vdt-ring-btn[data-ring="nakshatra"] { border-color: var(--vdt-nakshatra); color: var(--vdt-nakshatra); }
.vdt-ring-btn[data-ring="yoga"] { border-color: var(--vdt-yoga); color: var(--vdt-yoga); }
.vdt-ring-btn[data-ring="karana"] { border-color: var(--vdt-karana); color: var(--vdt-karana); }
.vdt-ring-btn.active { color: white; }
.vdt-ring-btn[data-ring="vaara"].active { background: var(--vdt-vaara); }
.vdt-ring-btn[data-ring="tithi"].active { background: var(--vdt-tithi); }
.vdt-ring-btn[data-ring="nakshatra"].active { background: var(--vdt-nakshatra); }
.vdt-ring-btn[data-ring="yoga"].active { background: var(--vdt-yoga); }
.vdt-ring-btn[data-ring="karana"].active { background: var(--vdt-karana); }
.vdt-ring-btn:hover { opacity: 0.85; transform: scale(1.02); }
.vdt-viz-body {
    display: grid;
    grid-template-columns: 1fr 300px;
    gap: var(--vdt-space-lg);
    padding: var(--vdt-space-lg);
}
@media (max-width: 800px) {
    .vdt-viz-body { grid-template-columns: 1fr; }
}
.vdt-chart-wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 400px;
    background: var(--vdt-bg-alt);
    border-radius: var(--vdt-radius);
    padding: var(--vdt-space-lg);
}
#vdtChart { max-width: 100%; }
.vdt-viz-details { display: flex; flex-direction: column; gap: var(--vdt-space-sm); }
.vdt-date-display {
    background: linear-gradient(135deg, var(--vdt-primary-bg), rgba(218, 165, 32, 0.05));
    border: 1px solid var(--vdt-primary-light);
    border-radius: var(--vdt-radius);
    padding: var(--vdt-space-md);
    text-align: center;
}
.vdt-date-display .label { 
    font-size: 0.7rem; 
    color: var(--vdt-primary-dark); 
    text-transform: uppercase;
    letter-spacing: 0.05em;
    font-weight: 600;
}
.vdt-date-display .value { 
    font-size: 1.15rem; 
    font-weight: 700; 
    color: var(--vdt-primary-dark);
    margin-top: 4px;
}
.vdt-date-picker {
    display: flex;
    align-items: center;
    gap: var(--vdt-space-sm);
    margin-top: var(--vdt-space-sm);
    justify-content: center;
}
.vdt-date-input {
    padding: 8px 12px;
    border: 1px solid var(--vdt-border);
    border-radius: var(--vdt-radius-sm);
    font-family: var(--vdt-font);
    font-size: 0.9rem;
    color: var(--vdt-text);
    background: var(--vdt-bg);
    cursor: pointer;
    transition: border-color 0.2s ease;
}
.vdt-date-input:hover,
.vdt-date-input:focus {
    border-color: var(--vdt-primary);
    outline: none;
}
.vdt-date-today-btn {
    padding: 8px 14px;
    border: 1px solid var(--vdt-primary-light);
    border-radius: var(--vdt-radius-sm);
    background: var(--vdt-primary-bg);
    color: var(--vdt-primary-dark);
    font-size: 0.8rem;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.2s ease;
}
.vdt-date-today-btn:hover {
    background: var(--vdt-primary-light);
    color: white;
}
.vdt-detail-row {
    display: flex;
    align-items: center;
    gap: var(--vdt-space-sm);
    padding: 10px 14px;
    background: var(--vdt-bg-alt);
    border-radius: var(--vdt-radius-sm);
    border-left: 4px solid;
    transition: all 0.2s ease;
}
.vdt-detail-row:hover { background: var(--vdt-bg); box-shadow: var(--vdt-shadow-sm); }
.vdt-detail-row[data-el="vaara"] { border-left-color: var(--vdt-vaara); }
.vdt-detail-row[data-el="tithi"] { border-left-color: var(--vdt-tithi); }
.vdt-detail-row[data-el="nakshatra"] { border-left-color: var(--vdt-nakshatra); }
.vdt-detail-row[data-el="yoga"] { border-left-color: var(--vdt-yoga); }
.vdt-detail-row[data-el="karana"] { border-left-color: var(--vdt-karana); }
.vdt-detail-row .icon { font-size: 1.2rem; width: 28px; text-align: center; }
.vdt-detail-row .info { flex: 1; }
.vdt-detail-row .info .label { 
    font-size: 0.7rem; 
    color: var(--vdt-text-muted); 
    text-transform: uppercase;
    letter-spacing: 0.03em;
}
.vdt-detail-row .info .value { font-weight: 600; font-size: 0.95rem; color: var(--vdt-text); }
.vdt-demo-notice {
    background: #fefce8;
    border: 1px solid #fde047;
    border-radius: var(--vdt-radius-sm);
    padding: 10px 14px;
    font-size: 0.8rem;
    color: #854d0e;
    text-align: center;
    margin-top: var(--vdt-space-sm);
}
.vdt-demo-notice strong { color: #713f12; }
.vdt-citations {
    background: var(--vdt-bg-alt);
    border-top: 1px solid var(--vdt-border);
}
.vdt-citation-card {
    background: var(--vdt-bg);
    border: 1px solid var(--vdt-border);
    border-left: 4px solid var(--vdt-primary);
    border-radius: var(--vdt-radius);
    padding: var(--vdt-space-lg);
    margin-bottom: var(--vdt-space-lg);
    box-shadow: var(--vdt-shadow-sm);
}
.vdt-citation-card:last-child { margin-bottom: 0; }
.vdt-citation-card h3 {
    display: flex;
    align-items: center;
    gap: 10px;
    color: var(--vdt-primary-dark);
    margin-bottom: var(--vdt-space-md);
    font-size: 1.1rem;
}
.vdt-citation-card h3 svg { width: 22px; height: 22px; }
.vdt-citation-text {
    font-family: var(--vdt-font-mono);
    font-size: 0.85rem;
    background: var(--vdt-bg-alt);
    border: 1px solid var(--vdt-border);
    padding: var(--vdt-space-md);
    border-radius: var(--vdt-radius-sm);
    color: var(--vdt-text-secondary);
    line-height: 1.75;
    white-space: pre-wrap;
    overflow-x: auto;
}
.vdt-citation-actions {
    display: flex;
    gap: var(--vdt-space-sm);
    margin-top: var(--vdt-space-md);
    flex-wrap: wrap;
}
.vdt-links {
    background: var(--vdt-bg);
    border-top: 1px solid var(--vdt-border);
}
.vdt-links-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: var(--vdt-space-md);
}
@media (max-width: 700px) {
    .vdt-links-grid { grid-template-columns: 1fr; }
}
.vdt-link-card {
    display: flex;
    align-items: center;
    gap: var(--vdt-space-md);
    padding: var(--vdt-space-lg);
    background: var(--vdt-bg);
    border: 1px solid var(--vdt-border);
    border-radius: var(--vdt-radius);
    text-decoration: none;
    color: inherit;
    transition: all 0.25s ease;
}
.vdt-link-card:hover { 
    border-color: var(--vdt-primary-light);
    box-shadow: var(--vdt-shadow-lg); 
    text-decoration: none;
    transform: translateY(-2px);
}
.vdt-link-icon {
    width: 48px;
    height: 48px;
    background: var(--vdt-primary-bg);
    border-radius: var(--vdt-radius);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    transition: all 0.25s ease;
}
.vdt-link-card:hover .vdt-link-icon { background: var(--vdt-primary-light); }
.vdt-link-icon svg { width: 24px; height: 24px; color: var(--vdt-primary-dark); }
.vdt-link-card:hover .vdt-link-icon svg { color: white; }
.vdt-link-content h3 { font-size: 1rem; color: var(--vdt-text); margin-bottom: 2px; }
.vdt-link-content p { font-size: 0.85rem; color: var(--vdt-text-muted); margin-bottom: 4px; }
.vdt-link-url { font-size: 0.75rem; color: var(--vdt-info); font-family: var(--vdt-font-mono); }
.vdt-footer {
    padding: var(--vdt-space-xl) 0;
    background: var(--vdt-bg-alt);
    border-top: 1px solid var(--vdt-border);
    text-align: center;
}
.vdt-footer p {
    font-size: 0.9rem;
    color: var(--vdt-text-muted);
    margin-bottom: var(--vdt-space-sm);
}
.vdt-footer p:last-child { margin-bottom: 0; }
.vdt-footer a { color: var(--vdt-primary-dark); }
.vdt-tooltip {
    position: fixed;
    background: var(--vdt-bg);
    border: 1px solid var(--vdt-border);
    padding: 10px 14px;
    border-radius: var(--vdt-radius-sm);
    box-shadow: var(--vdt-shadow-lg);
    pointer-events: none;
    z-index: 10000;
    max-width: 220px;
    font-size: 0.85rem;
    opacity: 0;
    transition: opacity 0.15s ease;
}
.vdt-tooltip.visible { opacity: 1; }
.vdt-tooltip-title { font-weight: 600; color: var(--vdt-text); margin-bottom: 2px; }
.vdt-tooltip-content { color: var(--vdt-text-muted); font-size: 0.8rem; }
</style>

<div class="vdt-showcase">
    <header class="vdt-header">
        <div class="vdt-container">
            <div class="vdt-header-logo">
                <img src="/assets/vedicdatetime/logo.png" alt="VedicDateTime Logo" class="vdt-logo" onerror="this.style.display='none'">
            </div>
            <div class="vdt-header-badge">
                <span class="vdt-badge">R Package on CRAN</span>
            </div>
            <h1>VedicDateTime</h1>
            <p class="vdt-header-tagline">
                Vedic Calendar System. An R package that implements traditional Vedic calendar calculations including Tithi, Nakshatra, Yoga, Karana, and more.
            </p>
            <div class="vdt-header-actions">
                <a href="https://cran.r-project.org/package=VedicDateTime" class="vdt-btn vdt-btn-primary" target="_blank" rel="noopener">
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4M7 10l5 5 5-5M12 15V3"/></svg>
                    Install from CRAN
                </a>
                <a href="https://github.com/neerajdhanraj/VedicDateTime" class="vdt-btn" target="_blank" rel="noopener">
                    <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                    View on GitHub
                </a>
            </div>
            <div class="vdt-header-meta">
                <div class="vdt-meta-item">
                    <div class="value">0.1.3</div>
                    <div class="label">Version</div>
                </div>
                <div class="vdt-meta-item">
                    <div class="value">GPL-3</div>
                    <div class="label">License</div>
                </div>
                <div class="vdt-meta-item">
                    <div class="value">5</div>
                    <div class="label">Panchanga Elements</div>
                </div>
                <div class="vdt-meta-item">
                    <div class="value">27</div>
                    <div class="label">Nakshatras</div>
                </div>
            </div>
        </div>
    </header>

    <section class="vdt-section vdt-overview" id="overview">
        <div class="vdt-container">
            <div class="vdt-overview-grid">
                <div class="vdt-overview-content">
                    <span class="vdt-label">About the Package</span>
                    <h2>Vedic Calendar System for R</h2>
                    <p>
                        VedicDateTime implements the traditional Vedic calendar system used in the Indian subcontinent. 
                        The package provides functions to calculate all five elements of the Panchanga (five limbs of time), 
                        enabling users to determine dates and timings based on traditional astronomical calculations.
                    </p>
                    <p>
                        Built on the Swiss Ephemeris for precise astronomical computations, VedicDateTime is useful for 
                        researchers, developers, and anyone interested in Vedic timekeeping and calendar systems.
                    </p>
                    <div class="vdt-pkg-meta">
                        <div class="vdt-pkg-meta-item">
                            <span class="label">Author</span>
                            <span class="value">Neeraj Dhanraj Bokde</span>
                        </div>
                        <div class="vdt-pkg-meta-item">
                            <span class="label">Published</span>
                            <span class="value">2022-04-27</span>
                        </div>
                        <div class="vdt-pkg-meta-item">
                            <span class="label">Maintainer</span>
                            <span class="value">neerajdhanraj@gmail.com</span>
                        </div>
                        <div class="vdt-pkg-meta-item">
                            <span class="label">Bug Reports</span>
                            <span class="value"><a href="https://github.com/neerajdhanraj/VedicDateTime/issues">GitHub Issues</a></span>
                        </div>
                    </div>
                </div>
                <div class="vdt-code-block">
                    <div class="vdt-code-header">
                        <div class="vdt-code-dots">
                            <span class="vdt-code-dot red"></span>
                            <span class="vdt-code-dot yellow"></span>
                            <span class="vdt-code-dot green"></span>
                        </div>
                        <span class="vdt-code-title">R Console</span>
                    </div>
                    <div class="vdt-code-body"><div class="code-line"><span class="comment"># Install from CRAN</span></div><div class="code-line"><span class="function">install.packages</span>(<span class="string">"VedicDateTime"</span>)</div><div class="code-line">&nbsp;</div><div class="code-line"><span class="comment"># Load the package</span></div><div class="code-line"><span class="function">library</span>(VedicDateTime)</div><div class="code-line">&nbsp;</div><div class="code-line"><span class="comment"># Get Panchanga elements for a date</span></div><div class="code-line">date <span class="keyword">&lt;-</span> <span class="function">as.Date</span>(<span class="string">"2024-01-15"</span>)</div><div class="code-line"><span class="function">tithi</span>(date)</div><div class="code-line"><span class="output">#&gt; [1] "Panchami"</span></div><div class="code-line"><span class="function">nakshatra</span>(date)</div><div class="code-line"><span class="output">#&gt; [1] "Rohini"</span></div><div class="code-line"><span class="function">vaara</span>(date)</div><div class="code-line"><span class="output">#&gt; [1] "Somvar"</span></div><div class="code-line"><span class="function">yoga</span>(date)</div><div class="code-line"><span class="output">#&gt; [1] "Saubhagya"</span></div><div class="code-line"><span class="function">karana</span>(date)</div><div class="code-line"><span class="output">#&gt; [1] "Taitila"</span></div></div>
                </div>
            </div>
        </div>
    </section>

    <section class="vdt-section vdt-features" id="features">
        <div class="vdt-container">
            <div class="vdt-section-header">
                <span class="vdt-label">Capabilities</span>
                <h2>Key Features</h2>
                <p>Calculate all five elements of the traditional Panchanga calendar system</p>
            </div>
            <div class="vdt-features-grid">
                <div class="vdt-feature-card">
                    <div class="vdt-feature-icon">&#x1F319;</div>
                    <h3>Tithi</h3>
                    <p>Calculate the lunar day based on the angular distance between Sun and Moon. 30 tithis per lunar month.</p>
                </div>
                <div class="vdt-feature-card">
                    <div class="vdt-feature-icon">&#x2B50;</div>
                    <h3>Nakshatra</h3>
                    <p>Determine which of the 27 lunar mansions the Moon currently occupies in the zodiac.</p>
                </div>
                <div class="vdt-feature-card">
                    <div class="vdt-feature-icon">&#x2600;</div>
                    <h3>Vaara</h3>
                    <p>Get the Vedic weekday name with its associated planetary deity and characteristics.</p>
                </div>
                <div class="vdt-feature-card">
                    <div class="vdt-feature-icon">&#x262F;</div>
                    <h3>Yoga</h3>
                    <p>Compute the 27 yogas formed by the combined longitudes of the Sun and Moon.</p>
                </div>
                <div class="vdt-feature-card">
                    <div class="vdt-feature-icon">&#x25D0;</div>
                    <h3>Karana</h3>
                    <p>Identify the half-tithi period. There are 11 karana types used in Vedic astrology.</p>
                </div>
                <div class="vdt-feature-card">
                    <div class="vdt-feature-icon">&#x1F4C5;</div>
                    <h3>Masa and Ritu</h3>
                    <p>Determine the lunar month and season classifications of the Vedic calendar.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="vdt-section vdt-viz" id="visualization">
        <div class="vdt-container">
            <div class="vdt-section-header">
                <span class="vdt-label">Interactive Demo</span>
                <h2>Panchanga Visualization</h2>
                <p>Explore the five elements of Vedic time through this interactive wheel</p>
            </div>
            <div class="vdt-viz-container">
                <div class="vdt-viz-header">
                    <div class="vdt-viz-title">
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>
                        <span>Panchanga Wheel</span>
                    </div>
                    <div class="vdt-viz-controls">
                        <button class="vdt-ring-btn active" data-ring="vaara" onclick="toggleRing('vaara')">Vaara</button>
                        <button class="vdt-ring-btn active" data-ring="tithi" onclick="toggleRing('tithi')">Tithi</button>
                        <button class="vdt-ring-btn active" data-ring="nakshatra" onclick="toggleRing('nakshatra')">Nakshatra</button>
                        <button class="vdt-ring-btn active" data-ring="yoga" onclick="toggleRing('yoga')">Yoga</button>
                        <button class="vdt-ring-btn active" data-ring="karana" onclick="toggleRing('karana')">Karana</button>
                    </div>
                </div>
                <div class="vdt-viz-body">
                    <div class="vdt-chart-wrapper">
                        <svg id="vdtChart" width="380" height="380" viewBox="0 0 380 380" role="img" aria-label="Panchanga radial chart"></svg>
                    </div>
                    <div class="vdt-viz-details">
                        <div class="vdt-date-display">
                            <div class="label">Select Date</div>
                            <div class="value" id="displayDate">January 15, 2024</div>
                            <div class="vdt-date-picker">
                                <input type="date" id="datePicker" class="vdt-date-input" value="2024-01-15">
                                <button class="vdt-date-today-btn" onclick="setToday()">Today</button>
                            </div>
                        </div>
                        <div class="vdt-detail-row" data-el="vaara">
                            <div class="icon">&#x2600;</div>
                            <div class="info"><div class="label">Vaara</div><div class="value" id="vaaraValue">Somvar (Monday)</div></div>
                        </div>
                        <div class="vdt-detail-row" data-el="tithi">
                            <div class="icon">&#x1F319;</div>
                            <div class="info"><div class="label">Tithi</div><div class="value" id="tithiValue">Panchami</div></div>
                        </div>
                        <div class="vdt-detail-row" data-el="nakshatra">
                            <div class="icon">&#x2B50;</div>
                            <div class="info"><div class="label">Nakshatra</div><div class="value" id="nakshatraValue">Rohini</div></div>
                        </div>
                        <div class="vdt-detail-row" data-el="yoga">
                            <div class="icon">&#x262F;</div>
                            <div class="info"><div class="label">Yoga</div><div class="value" id="yogaValue">Saubhagya</div></div>
                        </div>
                        <div class="vdt-detail-row" data-el="karana">
                            <div class="icon">&#x25D0;</div>
                            <div class="info"><div class="label">Karana</div><div class="value" id="karanaValue">Taitila</div></div>
                        </div>
                        <div class="vdt-demo-notice">
                            <strong>Demo Data:</strong> Values shown are illustrative. Use VedicDateTime for actual calculations.
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="vdt-section vdt-citations" id="citation">
        <div class="vdt-container">
            <div class="vdt-section-header">
                <span class="vdt-label">Attribution</span>
                <h2>How to Cite</h2>
                <p>If you use VedicDateTime in your research, please cite the package</p>
            </div>
            <div class="vdt-citation-card">
                <h3>
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>
                    Journal Article (Multimedia Tools and Applications)
                </h3>
                <div class="vdt-citation-text" id="articleCitation">Bokde, N.D., Patil, P., Sengupta, S., Sawant, M., &amp; Feijoo, A. (2023). 
VedicDateTime: An R package to implement Vedic calendar system.
Multimedia Tools and Applications.
https://doi.org/10.1007/s11042-023-16553-w</div>
                <div class="vdt-citation-actions">
                    <button class="vdt-btn" onclick="copyCitation('articleCitation')">
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="16" height="16"><rect x="9" y="9" width="13" height="13" rx="2"/><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"/></svg>
                        Copy
                    </button>
                    <a href="https://doi.org/10.1007/s11042-023-16553-w" class="vdt-btn" target="_blank" rel="noopener">
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="16" height="16"><path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"/><polyline points="15 3 21 3 21 9"/><line x1="10" y1="14" x2="21" y2="3"/></svg>
                        View Paper
                    </a>
                </div>
            </div>
            <div class="vdt-citation-card">
                <h3>
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/></svg>
                    R Package
                </h3>
                <div class="vdt-citation-text" id="pkgCitation">Bokde, N.D. (2022). VedicDateTime: Vedic Calendar System. 
R package version 0.1.3.
https://CRAN.R-project.org/package=VedicDateTime
DOI: 10.32614/CRAN.package.VedicDateTime</div>
                <div class="vdt-citation-actions">
                    <button class="vdt-btn" onclick="copyCitation('pkgCitation')">
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="16" height="16"><rect x="9" y="9" width="13" height="13" rx="2"/><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"/></svg>
                        Copy
                    </button>
                </div>
            </div>
            <div class="vdt-citation-card">
                <h3>
                    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>
                    BibTeX
                </h3>
                <div class="vdt-citation-text" id="bibtexCitation">@article{bokde2023vedicdatetime,
  title     = {VedicDateTime: An R package to implement 
               Vedic calendar system},
  author    = {Bokde, Neeraj Dhanraj and Patil, Prajwal and 
               Sengupta, Saradindu and Sawant, Mandar and 
               Feijoo, Andres},
  journal   = {Multimedia Tools and Applications},
  year      = {2023},
  publisher = {Springer},
  doi       = {10.1007/s11042-023-16553-w}
}</div>
                <div class="vdt-citation-actions">
                    <button class="vdt-btn" onclick="copyCitation('bibtexCitation')">
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="16" height="16"><rect x="9" y="9" width="13" height="13" rx="2"/><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h9a2 2 0 0 1 2 2v1"/></svg>
                        Copy BibTeX
                    </button>
                </div>
            </div>
        </div>
    </section>

    <section class="vdt-section vdt-links" id="links">
        <div class="vdt-container">
            <div class="vdt-section-header">
                <span class="vdt-label">Resources</span>
                <h2>Links</h2>
            </div>
            <div class="vdt-links-grid">
                <a href="https://cran.r-project.org/package=VedicDateTime" class="vdt-link-card" target="_blank" rel="noopener">
                    <div class="vdt-link-icon">
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
                    </div>
                    <div class="vdt-link-content">
                        <h3>CRAN</h3>
                        <p>Official R package repository</p>
                        <span class="vdt-link-url">cran.r-project.org/package=VedicDateTime</span>
                    </div>
                </a>
                <a href="https://github.com/neerajdhanraj/VedicDateTime" class="vdt-link-card" target="_blank" rel="noopener">
                    <div class="vdt-link-icon">
                        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
                    </div>
                    <div class="vdt-link-content">
                        <h3>GitHub</h3>
                        <p>Source code and issue tracker</p>
                        <span class="vdt-link-url">github.com/neerajdhanraj/VedicDateTime</span>
                    </div>
                </a>
                <a href="https://doi.org/10.1007/s11042-023-16553-w" class="vdt-link-card" target="_blank" rel="noopener">
                    <div class="vdt-link-icon">
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>
                    </div>
                    <div class="vdt-link-content">
                        <h3>Research Paper</h3>
                        <p>Multimedia Tools and Applications</p>
                        <span class="vdt-link-url">doi.org/10.1007/s11042-023-16553-w</span>
                    </div>
                </a>
                <a href="https://cran.r-project.org/web/packages/VedicDateTime/VedicDateTime.pdf" class="vdt-link-card" target="_blank" rel="noopener">
                    <div class="vdt-link-icon">
                        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M4 19.5A2.5 2.5 0 0 1 6.5 17H20"/><path d="M6.5 2H20v20H6.5A2.5 2.5 0 0 1 4 19.5v-15A2.5 2.5 0 0 1 6.5 2z"/></svg>
                    </div>
                    <div class="vdt-link-content">
                        <h3>Documentation</h3>
                        <p>Package reference manual</p>
                        <span class="vdt-link-url">CRAN PDF Manual</span>
                    </div>
                </a>
            </div>
        </div>
    </section>

    <footer class="vdt-footer">
        <div class="vdt-container">
            <p>&copy; 2022-2024 Neeraj Dhanraj Bokde. Released under the GPL-3 License.</p>
            <p>Maintainer: <a href="mailto:neerajdhanraj@gmail.com">neerajdhanraj@gmail.com</a></p>
        </div>
    </footer>
</div>

<div class="vdt-tooltip" id="vdtTooltip">
    <div class="vdt-tooltip-title"></div>
    <div class="vdt-tooltip-content"></div>
</div>

<script>
(function() {
    var VAARAS = [
        { name: "Ravivar", english: "Sunday", color: "#dc2626" },
        { name: "Somvar", english: "Monday", color: "#2563eb" },
        { name: "Mangalvar", english: "Tuesday", color: "#dc2626" },
        { name: "Budhvar", english: "Wednesday", color: "#059669" },
        { name: "Guruvar", english: "Thursday", color: "#d97706" },
        { name: "Shukravar", english: "Friday", color: "#7c3aed" },
        { name: "Shanivar", english: "Saturday", color: "#374151" }
    ];
    var TITHIS = ["Pratipada","Dwitiya","Tritiya","Chaturthi","Panchami","Shashthi","Saptami","Ashtami","Navami","Dashami","Ekadashi","Dwadashi","Trayodashi","Chaturdashi","Purnima/Amavasya"];
    var NAKSHATRAS = ["Ashwini","Bharani","Krittika","Rohini","Mrigashira","Ardra","Punarvasu","Pushya","Ashlesha","Magha","Purva Phalguni","Uttara Phalguni","Hasta","Chitra","Swati","Vishakha","Anuradha","Jyeshtha","Mula","Purva Ashadha","Uttara Ashadha","Shravana","Dhanishta","Shatabhisha","Purva Bhadrapada","Uttara Bhadrapada","Revati"];
    var YOGAS = ["Vishkumbha","Priti","Ayushman","Saubhagya","Shobhana","Atiganda","Sukarman","Dhriti","Shula","Ganda","Vriddhi","Dhruva","Vyaghata","Harshana","Vajra","Siddhi","Vyatipata","Variyan","Parigha","Shiva","Siddha","Sadhya","Shubha","Shukla","Brahma","Indra","Vaidhriti"];
    var KARANAS = ["Bava","Balava","Kaulava","Taitila","Gara","Vanija","Vishti","Shakuni","Chatushpada","Nagava","Kimstughna"];

    var RING_COLORS = {
        vaara: "#dc2626",
        tithi: "#0891b2",
        nakshatra: "#d97706",
        yoga: "#059669",
        karana: "#ea580c"
    };

    var selectedDate = "2024-01-15";
    var currentData = null;
    var visibleRings = { vaara: true, tithi: true, nakshatra: true, yoga: true, karana: true };

    function generatePanchangaForDate(dateStr) {
        var date = new Date(dateStr);
        var dayOfWeek = date.getDay();
        var dayOfMonth = date.getDate();
        var month = date.getMonth();
        var year = date.getFullYear();
        var tithiIndex = (dayOfMonth + month * 2) % 15;
        var nakshatraIndex = (dayOfMonth + month * 3 + Math.floor(year / 10)) % 27;
        var yogaIndex = (dayOfMonth * 2 + month + Math.floor(year / 100)) % 27;
        var karanaIndex = (dayOfMonth * 2 + month) % 11;
        return {
            vaara: dayOfWeek,
            tithi: { index: tithiIndex, name: TITHIS[tithiIndex] },
            nakshatra: { index: nakshatraIndex, name: NAKSHATRAS[nakshatraIndex] },
            yoga: { index: yogaIndex, name: YOGAS[yogaIndex] },
            karana: { index: karanaIndex, name: KARANAS[karanaIndex] }
        };
    }

    function polarToCartesian(cx, cy, r, angleRad) {
        return {
            x: cx + r * Math.cos(angleRad),
            y: cy + r * Math.sin(angleRad)
        };
    }

    function describeArc(cx, cy, innerR, outerR, startAngle, endAngle) {
        var startOuter = polarToCartesian(cx, cy, outerR, startAngle);
        var endOuter = polarToCartesian(cx, cy, outerR, endAngle);
        var startInner = polarToCartesian(cx, cy, innerR, startAngle);
        var endInner = polarToCartesian(cx, cy, innerR, endAngle);
        var largeArc = (endAngle - startAngle) > Math.PI ? 1 : 0;
        var d = [
            "M", startOuter.x, startOuter.y,
            "A", outerR, outerR, 0, largeArc, 1, endOuter.x, endOuter.y,
            "L", endInner.x, endInner.y,
            "A", innerR, innerR, 0, largeArc, 0, startInner.x, startInner.y,
            "Z"
        ].join(" ");
        return d;
    }

    function renderChart() {
        var svg = document.getElementById("vdtChart");
        if (!svg) return;
        
        var cx = 190, cy = 190;
        var html = [];
        
        html.push('<defs>');
        html.push('<radialGradient id="centerGradVDT" cx="50%" cy="50%" r="50%">');
        html.push('<stop offset="0%" style="stop-color:#b8860b;stop-opacity:0.25"/>');
        html.push('<stop offset="100%" style="stop-color:#ffffff;stop-opacity:0"/>');
        html.push('</radialGradient>');
        html.push('<filter id="glowVDT" x="-50%" y="-50%" width="200%" height="200%">');
        html.push('<feGaussianBlur stdDeviation="2" result="blur"/>');
        html.push('<feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>');
        html.push('</filter>');
        html.push('</defs>');
        
        var bgRadii = [175, 148, 118, 88, 58];
        for (var b = 0; b < bgRadii.length; b++) {
            html.push('<circle cx="' + cx + '" cy="' + cy + '" r="' + bgRadii[b] + '" fill="none" stroke="#e5e7eb" stroke-width="1" stroke-dasharray="2,2"/>');
        }
        
        var rings = [
            { key: "vaara", inner: 158, outer: 182, segments: 7, current: currentData.vaara, color: RING_COLORS.vaara, data: VAARAS },
            { key: "tithi", inner: 128, outer: 155, segments: 15, current: currentData.tithi.index, color: RING_COLORS.tithi, data: TITHIS },
            { key: "nakshatra", inner: 98, outer: 125, segments: 27, current: currentData.nakshatra.index, color: RING_COLORS.nakshatra, data: NAKSHATRAS },
            { key: "yoga", inner: 68, outer: 95, segments: 27, current: currentData.yoga.index, color: RING_COLORS.yoga, data: YOGAS },
            { key: "karana", inner: 40, outer: 65, segments: 11, current: currentData.karana.index, color: RING_COLORS.karana, data: KARANAS }
        ];
        
        for (var r = 0; r < rings.length; r++) {
            var ring = rings[r];
            if (!visibleRings[ring.key]) continue;
            
            var segmentAngle = (2 * Math.PI) / ring.segments;
            var gap = 0.02;
            
            for (var i = 0; i < ring.segments; i++) {
                var startAngle = i * segmentAngle - Math.PI / 2 + gap / 2;
                var endAngle = (i + 1) * segmentAngle - Math.PI / 2 - gap / 2;
                var isCurrent = (i === ring.current);
                var opacity = isCurrent ? 0.95 : 0.2;
                var strokeWidth = isCurrent ? 2 : 0.5;
                var strokeColor = isCurrent ? "#1f2937" : "#d1d5db";
                var path = describeArc(cx, cy, ring.inner, ring.outer, startAngle, endAngle);
                var segName = (ring.key === "vaara") ? ring.data[i].name : ring.data[i];
                var filterAttr = isCurrent ? ' filter="url(#glowVDT)"' : '';
                
                html.push('<path d="' + path + '" ');
                html.push('fill="' + ring.color + '" fill-opacity="' + opacity + '" ');
                html.push('stroke="' + strokeColor + '" stroke-width="' + strokeWidth + '"' + filterAttr + ' ');
                html.push('style="cursor:pointer;transition:all 0.2s ease" ');
                html.push('data-ring="' + ring.key + '" data-index="' + i + '" data-name="' + segName + '" data-current="' + isCurrent + '"/>');
            }
        }
        
        var vaaraColor = VAARAS[currentData.vaara].color;
        html.push('<circle cx="' + cx + '" cy="' + cy + '" r="36" fill="url(#centerGradVDT)" stroke="' + vaaraColor + '" stroke-width="3"/>');
        html.push('<text x="' + cx + '" y="' + (cy - 6) + '" text-anchor="middle" fill="' + vaaraColor + '" font-size="12" font-weight="700" font-family="system-ui, sans-serif">' + VAARAS[currentData.vaara].name + '</text>');
        html.push('<text x="' + cx + '" y="' + (cy + 10) + '" text-anchor="middle" fill="#6b7280" font-size="10" font-family="system-ui, sans-serif">' + VAARAS[currentData.vaara].english + '</text>');
        
        svg.innerHTML = html.join('');
        
        var paths = svg.querySelectorAll('path[data-ring]');
        paths.forEach(function(path) {
            path.addEventListener('mouseenter', function(e) {
                var name = e.target.getAttribute('data-name');
                var ringType = e.target.getAttribute('data-ring');
                var isCurrent = e.target.getAttribute('data-current') === 'true';
                showTooltip(e, name, ringType, isCurrent);
            });
            path.addEventListener('mouseleave', hideTooltip);
        });
    }

    function updateDetails() {
        var vaaraEl = document.getElementById("vaaraValue");
        var tithiEl = document.getElementById("tithiValue");
        var nakshatraEl = document.getElementById("nakshatraValue");
        var yogaEl = document.getElementById("yogaValue");
        var karanaEl = document.getElementById("karanaValue");
        
        if (vaaraEl) vaaraEl.textContent = VAARAS[currentData.vaara].name + " (" + VAARAS[currentData.vaara].english + ")";
        if (tithiEl) tithiEl.textContent = currentData.tithi.name;
        if (nakshatraEl) nakshatraEl.textContent = currentData.nakshatra.name;
        if (yogaEl) yogaEl.textContent = currentData.yoga.name;
        if (karanaEl) karanaEl.textContent = currentData.karana.name;
    }

    function updateDate(dateStr) {
        selectedDate = dateStr;
        currentData = generatePanchangaForDate(dateStr);
        var date = new Date(dateStr);
        var options = { year: "numeric", month: "long", day: "numeric" };
        var displayEl = document.getElementById("displayDate");
        var pickerEl = document.getElementById("datePicker");
        if (displayEl) displayEl.textContent = date.toLocaleDateString("en-US", options);
        if (pickerEl) pickerEl.value = dateStr;
        renderChart();
        updateDetails();
    }

    window.setToday = function() {
        var today = new Date();
        var y = today.getFullYear();
        var m = String(today.getMonth() + 1).padStart(2, '0');
        var d = String(today.getDate()).padStart(2, '0');
        updateDate(y + '-' + m + '-' + d);
    };

    window.toggleRing = function(ringName) {
        visibleRings[ringName] = !visibleRings[ringName];
        var btn = document.querySelector('.vdt-ring-btn[data-ring="' + ringName + '"]');
        if (btn) btn.classList.toggle("active");
        renderChart();
    };

    function showTooltip(event, name, type, isCurrent) {
        var tooltip = document.getElementById("vdtTooltip");
        if (!tooltip) return;
        tooltip.querySelector(".vdt-tooltip-title").textContent = name;
        tooltip.querySelector(".vdt-tooltip-content").innerHTML = 
            type.charAt(0).toUpperCase() + type.slice(1) + 
            (isCurrent ? ' <strong style="color:#059669">(Current)</strong>' : '');
        var x = event.clientX + 15;
        var y = event.clientY + 15;
        if (x + 220 > window.innerWidth) x = event.clientX - 230;
        if (y + 60 > window.innerHeight) y = event.clientY - 70;
        tooltip.style.left = x + "px";
        tooltip.style.top = y + "px";
        tooltip.classList.add("visible");
    }

    function hideTooltip() {
        var tooltip = document.getElementById("vdtTooltip");
        if (tooltip) tooltip.classList.remove("visible");
    }

    window.copyCitation = function(elementId) {
        var text = document.getElementById(elementId).textContent.trim();
        navigator.clipboard.writeText(text).then(function() {
            var btn = event.target.closest(".vdt-btn");
            var originalHTML = btn.innerHTML;
            btn.innerHTML = '<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" width="16" height="16"><path d="M22 11.08V12a10 10 0 1 1-5.93-9.14"/><polyline points="22 4 12 14.01 9 11.01"/></svg> Copied!';
            btn.style.color = "#059669";
            btn.style.borderColor = "#059669";
            setTimeout(function() {
                btn.innerHTML = originalHTML;
                btn.style.color = "";
                btn.style.borderColor = "";
            }, 1500);
        });
    };

    document.addEventListener("mousemove", function(e) {
        var tooltip = document.getElementById("vdtTooltip");
        if (tooltip && tooltip.classList.contains("visible")) {
            var x = e.clientX + 15;
            var y = e.clientY + 15;
            if (x + 220 > window.innerWidth) x = e.clientX - 230;
            if (y + 60 > window.innerHeight) y = e.clientY - 70;
            tooltip.style.left = x + "px";
            tooltip.style.top = y + "px";
        }
    });

    document.addEventListener("DOMContentLoaded", function() {
        currentData = generatePanchangaForDate(selectedDate);
        var picker = document.getElementById("datePicker");
        if (picker) {
            picker.addEventListener("change", function() {
                updateDate(this.value);
            });
        }
        renderChart();
        updateDetails();
    });
})();
</script>
