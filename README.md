<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>VK Lead Machine — AI-отдел продаж 24/7</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap');

  :root {
    --bg: #04070f;
    --bg2: #070c1a;
    --bg3: #0c1225;
    --card: #0f172a;
    --card2: #131e33;
    --border: #1e2d4a;
    --border2: #2a3f63;
    --accent: #00c2ff;
    --accent2: #7c3aed;
    --accent3: #f97316;
    --green: #10b981;
    --green2: #059669;
    --orange: #f97316;
    --orange2: #fb923c;
    --red: #ef4444;
    --pink: #ec4899;
    --gold: #f97316;
    --cyan: #00c2ff;
    --text: #e8edf5;
    --text2: #8fa3c0;
    --text3: #506070;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--bg);
    color: var(--text);
    overflow-x: hidden;
    line-height: 1.6;
  }

  ::-webkit-scrollbar { width: 5px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--border2); border-radius: 3px; }

  .container { max-width: 1140px; margin: 0 auto; padding: 0 32px; }

  /* ═══ BADGE ═══ */
  .badge {
    display: inline-flex; align-items: center; gap: 8px;
    padding: 6px 18px; border-radius: 100px;
    font-size: 12px; font-weight: 600; letter-spacing: 0.08em; text-transform: uppercase;
  }
  .badge-blue { background: rgba(0,194,255,0.10); border: 1px solid rgba(0,194,255,0.3); color: #67d9f7; }
  .badge-green { background: rgba(16,185,129,0.12); border: 1px solid rgba(16,185,129,0.3); color: #34d399; }
  .badge-red { background: rgba(239,68,68,0.12); border: 1px solid rgba(239,68,68,0.3); color: #f87171; }
  .badge-gold { background: rgba(249,115,22,0.12); border: 1px solid rgba(249,115,22,0.35); color: #fb923c; }
  .badge-purple { background: rgba(124,58,237,0.12); border: 1px solid rgba(124,58,237,0.3); color: #a78bfa; }

  /* ═══ HERO ═══ */
  .hero {
    min-height: 100vh;
    display: flex; align-items: center;
    position: relative; overflow: hidden;
  }

  .hero-bg {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 80% 60% at 10% 20%, rgba(0,194,255,0.12) 0%, transparent 50%),
      radial-gradient(ellipse 70% 50% at 90% 15%, rgba(249,115,22,0.10) 0%, transparent 45%),
      radial-gradient(ellipse 60% 70% at 80% 80%, rgba(124,58,237,0.14) 0%, transparent 50%),
      radial-gradient(ellipse 90% 40% at 40% 60%, rgba(124,58,237,0.06) 0%, transparent 60%),
      radial-gradient(ellipse 40% 30% at 20% 90%, rgba(0,194,255,0.07) 0%, transparent 40%);
  }

  .hero-grid {
    position: absolute; inset: 0;
    background-image:
      linear-gradient(rgba(35,47,72,0.5) 1px, transparent 1px),
      linear-gradient(90deg, rgba(35,47,72,0.5) 1px, transparent 1px);
    background-size: 60px 60px;
    mask-image: radial-gradient(ellipse 80% 80% at center, black 20%, transparent 75%);
  }

  .hero-particles {
    position: absolute; inset: 0; overflow: hidden;
  }
  .particle {
    position: absolute; width: 2px; height: 2px;
    background: var(--accent); border-radius: 50%;
    animation: float linear infinite;
    opacity: 0;
  }
  @keyframes float {
    0% { transform: translateY(100vh) translateX(0); opacity: 0; }
    10% { opacity: 0.6; }
    90% { opacity: 0.3; }
    100% { transform: translateY(-100px) translateX(40px); opacity: 0; }
  }

  .hero-content { position: relative; z-index: 2; width: 100%; text-align: center; padding: 100px 0 80px; }

  .hero-eyebrow {
    margin-bottom: 28px;
    display: flex; align-items: center; justify-content: center; gap: 12px; flex-wrap: wrap;
  }

  .hero-title {
    font-size: clamp(40px, 6vw, 80px);
    font-weight: 900;
    line-height: 1.05;
    letter-spacing: -0.03em;
    margin-bottom: 28px;
  }

  .title-gradient {
    background: linear-gradient(135deg, #00c2ff 0%, #7c3aed 35%, #f97316 65%, #00c2ff 100%);
    background-size: 200% auto;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: shine 4s linear infinite;
  }

  @keyframes shine {
    0% { background-position: 0% center; }
    100% { background-position: 200% center; }
  }

  .hero-sub {
    font-size: clamp(18px, 2.5vw, 26px);
    font-weight: 400;
    color: var(--text2);
    max-width: 760px;
    margin: 0 auto 48px;
    line-height: 1.5;
  }

  .hero-sub strong { color: var(--text); font-weight: 600; }

  .hero-stats {
    display: flex; align-items: center; justify-content: center; gap: 16px;
    flex-wrap: wrap; margin-bottom: 60px;
  }

  .hstat {
    display: flex; flex-direction: column; align-items: center;
    padding: 20px 32px;
    background: rgba(255,255,255,0.03);
    border: 1px solid var(--border);
    border-radius: 16px;
    min-width: 140px;
    transition: all 0.3s;
    position: relative; overflow: hidden;
  }
  .hstat::before {
    content: ''; position: absolute; inset: 0;
    background: linear-gradient(135deg, rgba(79,142,247,0.05), transparent);
    opacity: 0; transition: opacity 0.3s;
  }
  .hstat:hover { border-color: var(--orange); transform: translateY(-4px); }
  .hstat:hover::before { opacity: 1; }

  .hstat-num {
    font-size: 36px; font-weight: 900;
    background: linear-gradient(135deg, #00c2ff, #f97316);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    background-clip: text; line-height: 1;
    margin-bottom: 6px;
  }
  .hstat-label { font-size: 12px; color: var(--text3); text-transform: uppercase; letter-spacing: 0.06em; font-weight: 500; }

  .hero-divider { display: flex; align-items: center; justify-content: center; gap: 12px; color: var(--text3); font-size: 13px; margin-bottom: 60px; }
  .hero-divider::before, .hero-divider::after { content: ''; flex: 1; max-width: 120px; height: 1px; background: linear-gradient(90deg, transparent, var(--border2)); }
  .hero-divider::after { background: linear-gradient(90deg, var(--border2), transparent); }

  /* ═══ SECTION HEADER ═══ */
  .section-header {
    text-align: center; margin-bottom: 64px;
  }
  .section-header .badge { margin-bottom: 20px; }
  .section-title {
    font-size: clamp(30px, 4vw, 50px);
    font-weight: 800; letter-spacing: -0.02em;
    line-height: 1.15; margin-bottom: 16px;
  }
  .section-desc { font-size: 18px; color: var(--text2); max-width: 640px; margin: 0 auto; }

  /* ═══ PAIN SECTION ═══ */
  .pain-section {
    padding: 100px 0;
    background: linear-gradient(180deg, var(--bg) 0%, var(--bg2) 50%, var(--bg) 100%);
  }

  .pain-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 32px; margin-bottom: 60px;
  }

  .pain-card {
    padding: 36px;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 20px;
    position: relative; overflow: hidden;
  }

  .pain-card.bad {
    border-color: rgba(239,68,68,0.3);
    background: linear-gradient(135deg, rgba(239,68,68,0.05), var(--card));
  }
  .pain-card.bad::before {
    content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px;
    background: linear-gradient(90deg, #ef4444, #f97316);
  }

  .pain-icon { font-size: 40px; margin-bottom: 20px; display: block; }
  .pain-title { font-size: 22px; font-weight: 700; margin-bottom: 12px; }
  .pain-list { list-style: none; }
  .pain-list li {
    padding: 10px 0; border-bottom: 1px solid var(--border);
    display: flex; justify-content: space-between; align-items: center;
    font-size: 15px; color: var(--text2);
  }
  .pain-list li:last-child { border-bottom: none; }
  .pain-list .val { font-weight: 700; color: var(--red); font-size: 16px; }
  .pain-list .val.green { color: var(--green); }

  .pain-total {
    display: flex; justify-content: space-between; align-items: center;
    padding: 20px 24px;
    background: rgba(239,68,68,0.08);
    border: 1px solid rgba(239,68,68,0.3);
    border-radius: 12px;
    margin-top: 20px;
  }
  .pain-total-label { font-size: 16px; font-weight: 600; color: var(--text2); }
  .pain-total-val { font-size: 28px; font-weight: 900; color: var(--red); }

  /* ═══ COMPARISON TABLE ═══ */
  .compare-section { padding: 100px 0; }

  .compare-wrap {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 24px;
    overflow: hidden;
  }

  .compare-header {
    display: grid; grid-template-columns: 2fr 1fr 1fr;
    background: var(--bg3);
    border-bottom: 1px solid var(--border);
  }

  .ch-cell {
    padding: 24px 28px; font-size: 14px; font-weight: 700;
    text-transform: uppercase; letter-spacing: 0.06em;
  }
  .ch-cell.team { color: var(--red); }
  .ch-cell.ai {
    color: var(--green);
    background: rgba(16,185,129,0.05);
    border-left: 1px solid rgba(16,185,129,0.2);
    position: relative;
  }
  .ch-cell.ai::after {
    content: '★ ВЫБОР'; position: absolute; top: 8px; right: 12px;
    font-size: 9px; padding: 2px 8px;
    background: rgba(16,185,129,0.2); border-radius: 100px;
    color: var(--green);
  }

  .compare-row {
    display: grid; grid-template-columns: 2fr 1fr 1fr;
    border-bottom: 1px solid var(--border);
    transition: background 0.2s;
  }
  .compare-row:last-child { border-bottom: none; }
  .compare-row:hover { background: rgba(255,255,255,0.02); }

  .cr-cell {
    padding: 18px 28px; font-size: 15px;
    display: flex; align-items: center; gap: 10px;
  }
  .cr-cell.feature { color: var(--text2); font-weight: 500; }
  .cr-cell.team-val { color: var(--red); font-weight: 600; }
  .cr-cell.ai-val {
    color: var(--green); font-weight: 700;
    background: rgba(16,185,129,0.04);
    border-left: 1px solid rgba(16,185,129,0.15);
  }

  .cr-icon { font-size: 18px; flex-shrink: 0; }

  /* ═══ FUNNEL ═══ */
  .funnel-section {
    padding: 100px 0;
    background: linear-gradient(180deg, var(--bg) 0%, var(--bg2) 50%, var(--bg) 100%);
  }

  .funnel-steps {
    max-width: 800px; margin: 0 auto;
    display: flex; flex-direction: column; gap: 0;
    position: relative;
  }

  .funnel-steps::before {
    content: ''; position: absolute;
    left: 47px; top: 0; bottom: 0; width: 2px;
    background: linear-gradient(180deg, var(--accent), var(--accent2), var(--accent3));
  }

  .funnel-step {
    display: flex; gap: 28px; align-items: flex-start;
    padding: 32px 0;
    position: relative;
  }

  .step-num {
    width: 56px; height: 56px;
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 20px; font-weight: 900;
    flex-shrink: 0; position: relative; z-index: 1;
  }
  .step-num.s1 { background: linear-gradient(135deg, #4f8ef7, #2563eb); box-shadow: 0 0 20px rgba(79,142,247,0.4); }
  .step-num.s2 { background: linear-gradient(135deg, #7c3aed, #5b21b6); box-shadow: 0 0 20px rgba(124,58,237,0.4); }
  .step-num.s3 { background: linear-gradient(135deg, #06b6d4, #0891b2); box-shadow: 0 0 20px rgba(6,182,212,0.4); }
  .step-num.s4 { background: linear-gradient(135deg, #10b981, #059669); box-shadow: 0 0 20px rgba(16,185,129,0.4); }
  .step-num.s5 { background: linear-gradient(135deg, #f59e0b, #d97706); box-shadow: 0 0 20px rgba(245,158,11,0.4); }

  .step-body {
    flex: 1;
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 24px 28px;
    margin-top: 8px;
    transition: border-color 0.3s, transform 0.3s;
  }
  .step-body:hover { border-color: var(--border2); transform: translateX(4px); }

  .step-title { font-size: 18px; font-weight: 700; margin-bottom: 8px; }
  .step-desc { color: var(--text2); font-size: 14px; line-height: 1.6; }
  .step-meta {
    display: flex; gap: 12px; margin-top: 14px; flex-wrap: wrap;
  }
  .step-tag {
    padding: 4px 12px; border-radius: 100px;
    font-size: 11px; font-weight: 600; text-transform: uppercase; letter-spacing: 0.05em;
  }
  .step-tag.blue { background: rgba(79,142,247,0.1); color: #7fb3ff; border: 1px solid rgba(79,142,247,0.2); }
  .step-tag.green { background: rgba(16,185,129,0.1); color: #34d399; border: 1px solid rgba(16,185,129,0.2); }
  .step-tag.purple { background: rgba(124,58,237,0.1); color: #a78bfa; border: 1px solid rgba(124,58,237,0.2); }
  .step-tag.cyan { background: rgba(6,182,212,0.1); color: #67e8f9; border: 1px solid rgba(6,182,212,0.2); }
  .step-tag.gold { background: rgba(245,158,11,0.1); color: #fcd34d; border: 1px solid rgba(245,158,11,0.2); }

  /* ═══ METRICS ═══ */
  .metrics-section { padding: 100px 0; }

  .metrics-grid {
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 24px; margin-bottom: 64px;
  }

  .metric-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 36px 28px;
    position: relative; overflow: hidden;
    transition: all 0.3s;
  }

  .metric-card::before {
    content: ''; position: absolute;
    top: 0; left: 0; right: 0; height: 3px;
  }

  .metric-card.blue::before { background: linear-gradient(90deg, #00c2ff, #7c3aed); }
  .metric-card.green::before { background: linear-gradient(90deg, #10b981, #00c2ff); }
  .metric-card.gold::before { background: linear-gradient(90deg, #f97316, #7c3aed); }

  .metric-card:hover { transform: translateY(-6px); border-color: var(--border2); }

  .metric-icon { font-size: 36px; margin-bottom: 16px; }
  .metric-value {
    font-size: 52px; font-weight: 900; line-height: 1;
    margin-bottom: 8px; letter-spacing: -0.03em;
  }
  .metric-card.blue .metric-value { color: #00c2ff; }
  .metric-card.green .metric-value { color: var(--green); }
  .metric-card.gold .metric-value { color: #f97316; }

  .metric-label { font-size: 15px; font-weight: 600; color: var(--text); margin-bottom: 8px; }
  .metric-note { font-size: 13px; color: var(--text3); }

  /* ═══ ROI BLOCK ═══ */
  .roi-block {
    background: linear-gradient(135deg, rgba(16,185,129,0.08), rgba(6,182,212,0.05));
    border: 1px solid rgba(16,185,129,0.25);
    border-radius: 24px;
    padding: 52px;
    position: relative; overflow: hidden;
  }
  .roi-block::before {
    content: ''; position: absolute; inset: 0;
    background: radial-gradient(ellipse 60% 60% at 80% 50%, rgba(16,185,129,0.07), transparent);
  }

  .roi-content { position: relative; z-index: 1; }
  .roi-grid {
    display: grid; grid-template-columns: 1fr auto 1fr;
    gap: 40px; align-items: center;
  }

  .roi-side { }
  .roi-side-title { font-size: 13px; text-transform: uppercase; letter-spacing: 0.08em; color: var(--text3); font-weight: 600; margin-bottom: 20px; }

  .roi-cost {
    font-size: 56px; font-weight: 900; letter-spacing: -0.03em; line-height: 1;
    margin-bottom: 8px;
  }
  .roi-cost.red { color: var(--red); }
  .roi-cost.green { color: var(--green); }

  .roi-period { font-size: 14px; color: var(--text3); margin-bottom: 16px; }

  .roi-items { list-style: none; }
  .roi-items li {
    padding: 8px 0; font-size: 14px; color: var(--text2);
    display: flex; gap: 8px; align-items: center;
    border-bottom: 1px solid rgba(255,255,255,0.04);
  }
  .roi-items li:last-child { border-bottom: none; }
  .roi-items .ico { font-size: 16px; flex-shrink: 0; }

  .roi-vs {
    display: flex; flex-direction: column; align-items: center; gap: 8px;
  }
  .vs-circle {
    width: 80px; height: 80px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 18px; font-weight: 900;
    background: var(--bg3); border: 2px solid var(--border2);
    color: var(--text2); letter-spacing: -0.02em;
  }
  .vs-arrow { font-size: 28px; color: var(--green); }
  .vs-save {
    text-align: center;
    background: rgba(16,185,129,0.1); border: 1px solid rgba(16,185,129,0.3);
    border-radius: 12px; padding: 12px 20px;
  }
  .vs-save-num { font-size: 28px; font-weight: 900; color: var(--green); line-height: 1; }
  .vs-save-label { font-size: 11px; color: var(--green); text-transform: uppercase; letter-spacing: 0.06em; margin-top: 4px; }

  /* ═══ MODULES ═══ */
  .modules-section {
    padding: 100px 0;
    background: linear-gradient(180deg, var(--bg) 0%, var(--bg2) 50%, var(--bg) 100%);
  }

  .modules-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 28px; margin-bottom: 48px;
  }

  .module-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 24px;
    overflow: hidden;
    transition: all 0.3s;
  }
  .module-card:hover { transform: translateY(-6px); border-color: var(--border2); }

  .module-head {
    padding: 32px 32px 24px;
    position: relative;
  }
  .module-card.m1 .module-head { background: linear-gradient(135deg, rgba(79,142,247,0.1), rgba(124,58,237,0.05)); }
  .module-card.m2 .module-head { background: linear-gradient(135deg, rgba(16,185,129,0.1), rgba(6,182,212,0.05)); }

  .module-num {
    font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em;
    margin-bottom: 12px;
  }
  .module-card.m1 .module-num { color: var(--accent); }
  .module-card.m2 .module-num { color: var(--green); }

  .module-icon { font-size: 48px; margin-bottom: 16px; display: block; }
  .module-name { font-size: 22px; font-weight: 800; margin-bottom: 8px; }
  .module-tagline { font-size: 14px; color: var(--text2); }

  .module-body { padding: 24px 32px 32px; }
  .module-features { list-style: none; }
  .module-features li {
    padding: 11px 0;
    display: flex; gap: 12px; align-items: flex-start;
    border-bottom: 1px solid var(--border);
    font-size: 14px; color: var(--text2); line-height: 1.5;
  }
  .module-features li:last-child { border-bottom: none; }
  .mf-icon { font-size: 16px; flex-shrink: 0; margin-top: 1px; }

  .module-card.m1 .mf-icon { color: var(--accent); }
  .module-card.m2 .mf-icon { color: var(--green); }

  /* ═══ TOGETHER BLOCK ═══ */
  .together {
    background: linear-gradient(135deg, rgba(79,142,247,0.08), rgba(124,58,237,0.06), rgba(16,185,129,0.08));
    border: 1px solid var(--border2);
    border-radius: 24px;
    padding: 52px;
    text-align: center;
    position: relative; overflow: hidden;
  }
  .together::before {
    content: ''; position: absolute; inset: 0;
    background: radial-gradient(ellipse 60% 80% at 50% 50%, rgba(79,142,247,0.05), transparent);
  }
  .together-content { position: relative; z-index: 1; }
  .together-icons {
    display: flex; align-items: center; justify-content: center; gap: 20px;
    margin-bottom: 32px; font-size: 60px;
  }
  .t-plus { font-size: 32px; color: var(--text3); }
  .t-eq { font-size: 32px; color: var(--gold); }
  .together-title { font-size: 36px; font-weight: 900; margin-bottom: 16px; letter-spacing: -0.02em; }
  .together-desc { font-size: 18px; color: var(--text2); max-width: 680px; margin: 0 auto 32px; line-height: 1.6; }

  .together-pills {
    display: flex; flex-wrap: wrap; gap: 12px;
    justify-content: center;
  }
  .t-pill {
    padding: 10px 22px; border-radius: 100px;
    font-size: 13px; font-weight: 600;
    background: rgba(255,255,255,0.04);
    border: 1px solid var(--border2);
    color: var(--text2);
    transition: all 0.2s;
  }
  .t-pill:hover { background: rgba(79,142,247,0.1); border-color: var(--accent); color: var(--text); }

  /* ═══ GUARANTEE ═══ */
  .guarantee-section { padding: 100px 0; }

  .guarantees-grid {
    display: grid; grid-template-columns: repeat(4, 1fr);
    gap: 20px;
  }

  .g-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 20px;
    padding: 32px 24px;
    text-align: center;
    transition: all 0.3s;
  }
  .g-card:hover { border-color: var(--orange); transform: translateY(-4px); }

  .g-icon { font-size: 44px; margin-bottom: 16px; }
  .g-title { font-size: 16px; font-weight: 700; margin-bottom: 8px; }
  .g-desc { font-size: 13px; color: var(--text3); line-height: 1.5; }

  /* ═══ CTA ═══ */
  .cta-section {
    padding: 120px 0;
    position: relative; overflow: hidden;
  }

  .cta-bg {
    position: absolute; inset: 0;
    background:
      radial-gradient(ellipse 80% 60% at 50% 50%, rgba(79,142,247,0.1) 0%, transparent 60%),
      radial-gradient(ellipse 50% 50% at 20% 80%, rgba(124,58,237,0.08) 0%, transparent 50%),
      radial-gradient(ellipse 50% 50% at 80% 20%, rgba(6,182,212,0.06) 0%, transparent 50%);
  }

  .cta-content {
    position: relative; z-index: 1;
    text-align: center; max-width: 800px; margin: 0 auto;
  }

  .cta-title {
    font-size: clamp(36px, 5vw, 64px);
    font-weight: 900; line-height: 1.1; letter-spacing: -0.03em;
    margin-bottom: 24px;
  }

  .cta-sub { font-size: 20px; color: var(--text2); margin-bottom: 52px; line-height: 1.5; }

  .cta-box {
    background: var(--card2);
    border: 1px solid var(--border2);
    border-radius: 24px;
    padding: 48px;
    margin-bottom: 32px;
  }

  .cta-price-label { font-size: 13px; text-transform: uppercase; letter-spacing: 0.08em; color: var(--text3); margin-bottom: 12px; }
  .cta-price {
    font-size: 72px; font-weight: 900; letter-spacing: -0.04em; line-height: 1;
    background: linear-gradient(135deg, #00c2ff, #f97316);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 8px;
  }
  .cta-price-note { font-size: 14px; color: var(--text3); margin-bottom: 32px; }

  .cta-includes {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 12px; margin-bottom: 40px; text-align: left;
  }

  .ci-item {
    display: flex; gap: 10px; align-items: center;
    font-size: 14px; color: var(--text2);
  }
  .ci-check { color: var(--green); font-size: 16px; flex-shrink: 0; }

  .cta-btn {
    display: inline-flex; align-items: center; justify-content: center; gap: 10px;
    padding: 20px 52px; border-radius: 14px;
    font-size: 18px; font-weight: 700; color: white;
    background: linear-gradient(135deg, #00c2ff 0%, #7c3aed 40%, #f97316 70%, #00c2ff 100%);
    background-size: 200% auto;
    text-decoration: none; border: none; cursor: pointer;
    transition: all 0.3s;
    animation: btnshine 3s linear infinite;
    box-shadow: 0 8px 32px rgba(249,115,22,0.30), 0 4px 16px rgba(0,194,255,0.20);
    width: 100%;
  }
  .cta-btn:hover { transform: translateY(-3px); box-shadow: 0 12px 40px rgba(249,115,22,0.45), 0 6px 20px rgba(0,194,255,0.25); }
  @keyframes btnshine { 0% { background-position: 0% center; } 100% { background-position: 200% center; } }

  .cta-disclaimer { font-size: 13px; color: var(--text3); margin-top: 20px; }

  /* ═══ NAVBAR ═══ */
  .navbar {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(4,7,15,0.85);
    backdrop-filter: blur(20px);
    border-bottom: 1px solid rgba(0,194,255,0.12);
    padding: 0;
  }
  .navbar-inner {
    max-width: 1140px; margin: 0 auto; padding: 0 32px;
    height: 64px;
    display: flex; align-items: center; justify-content: space-between;
  }
  .navbar-logo {
    display: flex; align-items: center; gap: 12px;
    text-decoration: none;
  }
  .navbar-logo img {
    height: 40px; width: auto;
    border-radius: 8px;
  }
  .navbar-brand {
    display: flex; flex-direction: column;
  }
  .navbar-name {
    font-size: 20px; font-weight: 900; letter-spacing: 0.04em;
    background: linear-gradient(135deg, #00c2ff, #f97316);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    background-clip: text; line-height: 1;
  }
  .navbar-tagline {
    font-size: 10px; color: var(--text3); text-transform: uppercase;
    letter-spacing: 0.1em; margin-top: 2px;
  }
  .navbar-product {
    font-size: 13px; font-weight: 600;
    color: var(--text2);
    background: rgba(0,194,255,0.08);
    border: 1px solid rgba(0,194,255,0.2);
    padding: 6px 16px; border-radius: 100px;
  }
  .navbar-product span {
    color: #00c2ff;
  }

  /* ═══ FOOTER ═══ */
  footer {
    border-top: 1px solid rgba(0,194,255,0.12);
    padding: 48px 0 32px;
    text-align: center;
    color: var(--text3); font-size: 13px;
    background: linear-gradient(180deg, var(--bg) 0%, var(--bg2) 100%);
  }
  .footer-logo {
    display: flex; align-items: center; justify-content: center; gap: 14px;
    margin-bottom: 20px;
  }
  .footer-logo img { height: 48px; border-radius: 10px; }
  .footer-brand-name {
    font-size: 28px; font-weight: 900; letter-spacing: 0.05em;
    background: linear-gradient(135deg, #00c2ff, #f97316);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
    background-clip: text; line-height: 1;
  }
  .footer-brand-sub {
    font-size: 11px; color: var(--text3); text-transform: uppercase; letter-spacing: 0.1em; margin-top: 3px;
  }
  footer strong { color: var(--text2); }

  /* ═══ DIVIDER ═══ */
  .section-divider {
    height: 1px; background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 0;
  }

  /* ═══ RESPONSIVE ═══ */
  @media (max-width: 900px) {
    .pain-grid, .modules-grid, .roi-grid, .metrics-grid, .guarantees-grid { grid-template-columns: 1fr; }
    .roi-grid { text-align: center; }
    .compare-header, .compare-row { grid-template-columns: 1fr; }
    .ch-cell.team, .ch-cell.ai, .cr-cell.team-val, .cr-cell.ai-val { border-left: none; }
    .cta-includes { grid-template-columns: 1fr; }
    .roi-block, .together, .cta-box { padding: 32px 24px; }
    .hero-stats { gap: 10px; }
    .hstat { padding: 16px 20px; min-width: 110px; }
  }

  /* ═══ PRINT / PDF ═══ */
  @media print {
    body { background: #fff !important; color: #000 !important; }
    .hero-bg, .hero-grid, .hero-particles, .cta-bg { display: none; }
    section { padding: 40px 0; page-break-inside: avoid; }
    .hero { min-height: auto; padding: 60px 0; }
  }
</style>
</head>
<body>

<!-- ════════════════════════════════════════════
     NAVBAR
════════════════════════════════════════════ -->
<nav class="navbar">
  <div class="navbar-inner">
    <a href="#" class="navbar-logo">
      <img src="logo-full.jpg" alt="АТОМ">
      <div class="navbar-brand">
        <div class="navbar-name">АТОМ</div>
        <div class="navbar-tagline">Интеграция ИИ в бизнес</div>
      </div>
    </a>
    <div class="navbar-product">🚀 <span>VK Lead Machine Pro</span></div>
  </div>
</nav>

<!-- ════════════════════════════════════════════
     HERO
════════════════════════════════════════════ -->
<section class="hero" style="padding-top: 64px;">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-particles" id="particles"></div>

  <div class="container">
    <div class="hero-content">

      <!-- Логотип АТОМ -->
      <div style="margin-bottom: 32px; display: flex; flex-direction: column; align-items: center; gap: 12px;">
        <img src="logo-full.jpg" alt="АТОМ — Интеграция ИИ в бизнес"
             style="height: 100px; width: auto; border-radius: 16px; box-shadow: 0 0 40px rgba(0,194,255,0.20), 0 0 20px rgba(249,115,22,0.15);">
      </div>

      <div class="hero-eyebrow">
        <span class="badge badge-blue">⚡ АТОМ — Интеграция ИИ в бизнес</span>
        <span class="badge badge-gold">🚀 VK Lead Machine Pro</span>
      </div>

      <h1 class="hero-title">
        Ваш отдел продаж<br>
        <span class="title-gradient">работает 24/7<br>без зарплаты</span>
      </h1>

      <p class="hero-sub">
        Единая AI-система, которая <strong>сама находит клиентов</strong> во ВКонтакте,<br>
        <strong>сама пишет им</strong> и <strong>сама доводит до сделки</strong> — пока вы занимаетесь бизнесом
      </p>

      <div class="hero-stats">
        <div class="hstat">
          <div class="hstat-num">24/7</div>
          <div class="hstat-label">без выходных</div>
        </div>
        <div class="hstat">
          <div class="hstat-num">500+</div>
          <div class="hstat-label">лидов в месяц</div>
        </div>
        <div class="hstat">
          <div class="hstat-num">−90%</div>
          <div class="hstat-label">сокращение расходов на маркетинг</div>
        </div>
        <div class="hstat">
          <div class="hstat-num">5 мин</div>
          <div class="hstat-label">реакция на ответ</div>
        </div>
        <div class="hstat">
          <div class="hstat-num">ROI</div>
          <div class="hstat-label">с первого месяца</div>
        </div>
      </div>

      <div class="hero-divider">
        прокрутите вниз, чтобы узнать детали
      </div>

    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- ════════════════════════════════════════════
     PAIN — СКОЛЬКО ВЫ ПЛАТИТЕ СЕЙЧАС
════════════════════════════════════════════ -->
<section class="pain-section">
  <div class="container">
    <div class="section-header">
      <span class="badge badge-red">💸 Реальные цифры</span>
      <h2 class="section-title">Сколько стоит<br><span class="title-gradient">искать клиентов по-старому?</span></h2>
      <p class="section-desc">Посчитайте, во сколько обходится стандартная команда для лидогенерации в VK</p>
    </div>

    <div class="pain-grid">
      <div class="pain-card bad">
        <span class="pain-icon">👥</span>
        <h3 class="pain-title">Команда сотрудников</h3>
        <ul class="pain-list">
          <li><span>SMM-менеджер</span> <span class="val">80 000 ₽/мес</span></li>
          <li><span>Контекстная реклама (Яндекс.Директ)</span> <span class="val">от 50 000 ₽ на тесты</span></li>
          <li><span>Таргет VK Ads (риск слива бюджета)</span> <span class="val">от 50 000 ₽/мес</span></li>
          <li><span>Копирайтер / Дизайнер</span> <span class="val">40 000 ₽/мес</span></li>
          <li><span>Потери на нецелевые клики (CPC 50–300 ₽)</span> <span class="val">непредсказуемо</span></li>
          <li><span>Человеческий фактор, текучка, отпуска</span> <span class="val">постоянно</span></li>
        </ul>
        <div class="pain-total">
          <span class="pain-total-label">🔴 Итого ежемесячно</span>
          <span class="pain-total-val">от 270 000 ₽</span>
        </div>
      </div>

      <div class="pain-card">
        <span class="pain-icon">🤖</span>
        <h3 class="pain-title">VK Lead Machine</h3>
        <ul class="pain-list">
          <li><span>Анализирует аудиторию — сам</span> <span class="val green">✓</span></li>
          <li><span>Находит горячих лидов — сам</span> <span class="val green">✓</span></li>
          <li><span>Пишет комментарии — сам</span> <span class="val green">✓</span></li>
          <li><span>Ведёт диалог в ЛС — сам</span> <span class="val green">✓</span></li>
          <li><span>API & Хостинг (n8n + AI-модели)</span> <span class="val green">~5 000–10 000 ₽/мес</span></li>
          <li><span>Зарплаты, реклама, агентства</span> <span class="val green">0 ₽</span></li>
        </ul>
        <div class="pain-total" style="background: rgba(16,185,129,0.08); border-color: rgba(16,185,129,0.3);">
          <span class="pain-total-label" style="color: var(--text2);">🟢 Расходы ежемесячно</span>
          <span class="pain-total-val" style="color: var(--green);">~15 000 ₽/мес</span>
        </div>
      </div>
    </div>

    <!-- Дополнительные боли -->
    <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; margin-top: 16px;">

      <div style="background: var(--card); border: 1px solid var(--border); border-radius: 16px; padding: 28px; text-align: center;">
        <div style="font-size: 40px; margin-bottom: 12px;">😤</div>
        <div style="font-size: 15px; font-weight: 700; margin-bottom: 8px;">Человеческий фактор</div>
        <div style="font-size: 13px; color: var(--text3); line-height: 1.5;">Менеджер устал — написал плохо. Встал не с той ноги — упустил тёплого лида. Заболел — воронка встала</div>
      </div>

      <div style="background: var(--card); border: 1px solid var(--border); border-radius: 16px; padding: 28px; text-align: center;">
        <div style="font-size: 40px; margin-bottom: 12px;">⏰</div>
        <div style="font-size: 15px; font-weight: 700; margin-bottom: 8px;">Время ответа</div>
        <div style="font-size: 13px; color: var(--text3); line-height: 1.5;">Человек пишет ночью или в выходной — ответа нет. Остыл, ушёл к конкурентам. AI отвечает через 5 минут</div>
      </div>

      <div style="background: var(--card); border: 1px solid var(--border); border-radius: 16px; padding: 28px; text-align: center;">
        <div style="font-size: 40px; margin-bottom: 12px;">📉</div>
        <div style="font-size: 15px; font-weight: 700; margin-bottom: 8px;">Непредсказуемость</div>
        <div style="font-size: 13px; color: var(--text3); line-height: 1.5;">Сотрудник уходит — теряете наработки, контакты, воронку. Система никуда не уходит и помнит всё</div>
      </div>

    </div>

  </div>
</section>

<div class="section-divider"></div>

<!-- ════════════════════════════════════════════
     COMPARISON TABLE
════════════════════════════════════════════ -->
<section class="compare-section">
  <div class="container">
    <div class="section-header">
      <span class="badge badge-purple">📊 Сравнение</span>
      <h2 class="section-title">Команда из 4 человек<br><span class="title-gradient">против одной системы</span></h2>
      <p class="section-desc">Факты без прикрас — цифры, которые говорят сами за себя</p>
    </div>

    <div class="compare-wrap">
      <div class="compare-header">
        <div class="ch-cell">Параметр</div>
        <div class="ch-cell team">👥 Команда людей</div>
        <div class="ch-cell ai">🤖 VK Lead Machine</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">💰</span> Ежемесячные расходы</div>
        <div class="cr-cell team-val">от 270 000 ₽/мес</div>
        <div class="cr-cell ai-val">~15 000 ₽/мес (API + хостинг)</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">⏱️</span> Рабочие часы в месяц</div>
        <div class="cr-cell team-val">~640 часов (8ч × 4 чел × 20 дней)</div>
        <div class="cr-cell ai-val">720 часов — всегда 24/7</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">🎯</span> Лидов в месяц (потенциал)</div>
        <div class="cr-cell team-val">100–200 лидов</div>
        <div class="cr-cell ai-val">300–700 лидов</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">⚡</span> Скорость реакции на ответ</div>
        <div class="cr-cell team-val">от 30 минут до нескольких часов</div>
        <div class="cr-cell ai-val">до 5 минут круглосуточно</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">📊</span> Аналитика эффективности</div>
        <div class="cr-cell team-val">ручные отчёты, раз в неделю</div>
        <div class="cr-cell ai-val">Google Sheets в реальном времени</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">🎨</span> Качество текстов</div>
        <div class="cr-cell team-val">зависит от настроения, усталости</div>
        <div class="cr-cell ai-val">одинаково высокое всегда</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">🔄</span> Масштабирование</div>
        <div class="cr-cell team-val">нанять новых — ещё +100 000 ₽/мес</div>
        <div class="cr-cell ai-val">меняем лимит в Config — бесплатно</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">🏖️</span> Отпуска, больничные</div>
        <div class="cr-cell team-val">обязательно оплачиваются по закону</div>
        <div class="cr-cell ai-val">не существуют</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">🧠</span> Запоминание контекста</div>
        <div class="cr-cell team-val">может забыть, перепутать, потерять</div>
        <div class="cr-cell ai-val">полная история каждого диалога</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">📱</span> Работа в выходные</div>
        <div class="cr-cell team-val">доп. оплата или отказ</div>
        <div class="cr-cell ai-val">пн = пт = вс = праздники — без разницы</div>
      </div>

      <div class="compare-row">
        <div class="cr-cell feature"><span class="cr-icon">👋</span> Риск увольнения / ухода</div>
        <div class="cr-cell team-val">высокий, особенно менеджеры продаж</div>
        <div class="cr-cell ai-val">нулевой — система ваша навсегда</div>
      </div>

    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- ════════════════════════════════════════════
     FUNNEL — КАК РАБОТАЕТ
════════════════════════════════════════════ -->
<section class="funnel-section">
  <div class="container">
    <div class="section-header">
      <span class="badge badge-blue">🔄 Воронка продаж</span>
      <h2 class="section-title">От незнакомца<br><span class="title-gradient">до горячей заявки</span></h2>
      <p class="section-desc">Система проходит весь путь автоматически — от анализа рынка до момента, когда менеджер получает готового клиента</p>
    </div>

    <div class="funnel-steps">

      <div class="funnel-step">
        <div class="step-num s1">1</div>
        <div class="step-body">
          <div class="step-title">🔍 Изучает рынок и аудиторию</div>
          <div class="step-desc">
            AI анализирует ваш бизнес, продукт и целевую аудиторию. Автоматически генерирует десятки поисковых запросов, по которым ищет ВКонтакте людей, которым нужны именно ваши услуги. Использует данные Яндекс.Вордстат — самого большого поискового индекса рунета.
          </div>
          <div class="step-meta">
            <span class="step-tag blue">Раз в сутки</span>
            <span class="step-tag blue">Яндекс.Вордстат</span>
            <span class="step-tag blue">AI-анализ</span>
          </div>
        </div>
      </div>

      <div class="funnel-step">
        <div class="step-num s2">2</div>
        <div class="step-body">
          <div class="step-title">🎯 Находит тёплых лидов с AI-скорингом</div>
          <div class="step-desc">
            Каждые 15 минут система сканирует VK-группы с вашей целевой аудиторией. Для каждого активного пользователя AI выставляет оценку релевантности от 0 до 100 — учитывается активность, тематика постов, поведение в группах. В базу попадают только реально заинтересованные люди.
          </div>
          <div class="step-meta">
            <span class="step-tag purple">Каждые 15 мин</span>
            <span class="step-tag purple">AI-скоринг 0–100</span>
            <span class="step-tag purple">Фильтрация мусора</span>
          </div>
        </div>
      </div>

      <div class="funnel-step">
        <div class="step-num s3">3</div>
        <div class="step-body">
          <div class="step-title">✍️ Пишет нативные комментарии</div>
          <div class="step-desc">
            AI генерирует уникальный комментарий к каждому посту — под тему обсуждения, без рекламного tone-of-voice. Человек видит полезный ответ, а не спам. Это создаёт первый органический контакт, который не вызывает отторжения.
          </div>
          <div class="step-meta">
            <span class="step-tag cyan">Каждые 20 мин</span>
            <span class="step-tag cyan">Нативный контент</span>
            <span class="step-tag cyan">До 100 комментариев/день</span>
          </div>
        </div>
      </div>

      <div class="funnel-step">
        <div class="step-num s4">4</div>
        <div class="step-body">
          <div class="step-title">💬 Переводит в личные сообщения</div>
          <div class="step-desc">
            Когда человек отвечает на комментарий — система мгновенно это замечает и начинает диалог в личке. Первое сообщение отправляется в тот же момент, пока интерес горячий. Конкуренты узнают об этом потенциальном клиенте только завтра.
          </div>
          <div class="step-meta">
            <span class="step-tag green">Каждые 10 мин</span>
            <span class="step-tag green">Моментальная реакция</span>
            <span class="step-tag green">До 20 новых диалогов/день</span>
          </div>
        </div>
      </div>

      <div class="funnel-step">
        <div class="step-num s5">5</div>
        <div class="step-body">
          <div class="step-title">🏆 Доводит до заявки и передаёт менеджеру</div>
          <div class="step-desc">
            AI ведёт диалог по воронке продаж: установление контакта → выявление потребности → квалификация → закрытие. Помнит весь контекст разговора. Когда человек готов — отправляет уведомление менеджеру в Telegram с полным досье: кто, откуда, о чём говорили.
          </div>
          <div class="step-meta">
            <span class="step-tag gold">Каждые 5 мин</span>
            <span class="step-tag gold">Воронка продаж</span>
            <span class="step-tag gold">Передача менеджеру</span>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- ════════════════════════════════════════════
     METRICS
════════════════════════════════════════════ -->
<section class="metrics-section">
  <div class="container">
    <div class="section-header">
      <span class="badge badge-green">📈 Цифры системы</span>
      <h2 class="section-title">Производительность,<br><span class="title-gradient">которую не купить за зарплату</span></h2>
    </div>

    <div class="metrics-grid">

      <div class="metric-card blue">
        <div class="metric-icon">🕐</div>
        <div class="metric-value">8 760</div>
        <div class="metric-label">часов работы в год</div>
        <div class="metric-note">Сотрудник — 1 984 рабочих часа. Разница в 4,4 раза</div>
      </div>

      <div class="metric-card green">
        <div class="metric-icon">🎯</div>
        <div class="metric-value">500+</div>
        <div class="metric-label">лидов в месяц (потенциал)</div>
        <div class="metric-note">Зависит от ниши и аудитории. Средний менеджер — 80–120</div>
      </div>

      <div class="metric-card gold">
        <div class="metric-icon">⚡</div>
        <div class="metric-value">&lt;5 мин</div>
        <div class="metric-label">время реакции на ответ</div>
        <div class="metric-note">Среднее время ответа менеджера — 47 минут по статистике HubSpot</div>
      </div>

      <div class="metric-card blue">
        <div class="metric-icon">🧠</div>
        <div class="metric-value">100%</div>
        <div class="metric-label">сохранность истории диалогов</div>
        <div class="metric-note">Каждое сообщение, каждый контакт — в Google Sheets навсегда</div>
      </div>

      <div class="metric-card green">
        <div class="metric-icon">📊</div>
        <div class="metric-value">12</div>
        <div class="metric-label">таблиц аналитики в реальном времени</div>
        <div class="metric-note">Лиды, воронка, диалоги, статистика, ошибки — всё под контролем</div>
      </div>

      <div class="metric-card gold">
        <div class="metric-icon">🔄</div>
        <div class="metric-value">5</div>
        <div class="metric-label">параллельных AI-процессов</div>
        <div class="metric-note">Анализ, парсинг, комментарии, мониторинг, диалоги — всё одновременно</div>
      </div>

    </div>

    <!-- ROI BLOCK -->
    <div class="roi-block">
      <div class="roi-content">
        <div style="text-align: center; margin-bottom: 40px;">
          <span class="badge badge-green" style="margin-bottom: 16px;">💰 Финансовая математика</span>
          <h3 style="font-size: 32px; font-weight: 800; letter-spacing: -0.02em;">Окупаемость с первого месяца</h3>
        </div>

        <div class="roi-grid">

          <div class="roi-side">
            <div class="roi-side-title">❌ Традиционный маркетинг (в месяц)</div>
            <div class="roi-cost red">270 000 ₽</div>
            <div class="roi-period">ежемесячно × 12 = 3 240 000 ₽/год</div>
            <ul class="roi-items">
              <li><span class="ico">👤</span> SMM-менеджер: 80 000 ₽</li>
              <li><span class="ico">📢</span> Контекстная / таргет реклама: 150 000 ₽</li>
              <li><span class="ico">✏️</span> Копирайтер / Дизайнер: 40 000 ₽</li>
              <li><span class="ico">💸</span> Нецелевые клики (CPC 50–300 ₽): слив</li>
              <li><span class="ico">🔄</span> Текучка, обучение, человеческий фактор</li>
              <li><span class="ico">📉</span> Стоимость лида в 3–5 раз выше</li>
            </ul>
          </div>

          <div class="roi-vs">
            <div class="vs-circle">VS</div>
            <div class="vs-arrow">↓</div>
            <div class="vs-save">
              <div class="vs-save-num">3 млн</div>
              <div class="vs-save-label">экономия в год</div>
            </div>
            <div class="vs-arrow">↓</div>
            <div style="text-align: center; padding: 12px 16px; background: rgba(251,191,36,0.1); border: 1px solid rgba(251,191,36,0.3); border-radius: 12px;">
              <div style="font-size: 22px; font-weight: 900; color: var(--gold); line-height: 1;">−90%</div>
              <div style="font-size: 11px; color: var(--gold); text-transform: uppercase; letter-spacing: 0.06em; margin-top: 4px;">сокращение расходов</div>
            </div>
          </div>

          <div class="roi-side">
            <div class="roi-side-title">✅ С VK Lead Machine (в месяц)</div>
            <div class="roi-cost green">~15 000 ₽</div>
            <div class="roi-period">API + хостинг n8n + AI-модели — и больше ничего</div>
            <ul class="roi-items">
              <li><span class="ico">🤖</span> Зарплаты сотрудников: 0 ₽</li>
              <li><span class="ico">📢</span> Реклама и таргет: 0 ₽ (органика)</li>
              <li><span class="ico">✏️</span> Копирайтер / Дизайнер: 0 ₽ (делает ИИ)</li>
              <li><span class="ico">♾️</span> Работает бесконечно после настройки</li>
              <li><span class="ico">📊</span> Стоимость лида снижается в 3–5 раз</li>
              <li><span class="ico">🏆</span> Окупаемость внедрения: 1.5–3 месяца</li>
            </ul>
          </div>

        </div>
      </div>
    </div>

  </div>
</section>

<div class="section-divider"></div>

<!-- ════════════════════════════════════════════
     MODULES — ЧТО ВХОДИТ В СИСТЕМУ
════════════════════════════════════════════ -->
<section class="modules-section">
  <div class="container">
    <div class="section-header">
      <span class="badge badge-purple">🧩 Состав системы</span>
      <h2 class="section-title">Два мощных модуля —<br><span class="title-gradient">одна непрерывная машина</span></h2>
      <p class="section-desc">Каждый модуль решает свою задачу. Вместе они создают замкнутую систему от анализа до продажи</p>
    </div>

    <div class="modules-grid">

      <!-- Module 1 -->
      <div class="module-card m1">
        <div class="module-head">
          <div class="module-num">Модуль 01 · Разведка рынка</div>
          <span class="module-icon">🔬</span>
          <div class="module-name">Wordstat Intelligence</div>
          <div class="module-tagline">Понимает, как ваша аудитория ищет вас в интернете, и находит её там</div>
        </div>
        <div class="module-body">
          <ul class="module-features">
            <li>
              <span class="mf-icon">▶</span>
              <span><strong>Двойная семантика Яндекс + VK:</strong> анализирует ключи не только в Яндекс.Вордстат, но и внутри ВКонтакте — находит неочевидные запросы, по которым ваша аудитория ищет контент прямо в ленте</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span><strong>Попадание в рекомендации ВК:</strong> определяет идеальные ключи, хэштеги и структуру поста — система знает, какой контент алгоритм ВКонтакте продвигает в «Интересное» и раздел рекомендаций</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span><strong>SEO-индексация в Яндексе:</strong> оптимизирует посты под поисковые алгоритмы — ваш контент появляется в органической выдаче Яндекса по широким запросам и создаёт «вечный» трафик без рекламного бюджета</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span>Автоматически генерирует 150–300 ключевых запросов под ваш бизнес — без участия маркетолога и SEO-специалиста</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span>Анализирует топ-200 конкурентных постов по engagement rate — определяет идеальное время, формат и длину поста для максимального охвата</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span>Обновляется каждые 6 часов — база ключей всегда актуальна, тренды не пропускаются, алгоритмы платформ учитываются в реальном времени</span>
            </li>
          </ul>
        </div>
      </div>

      <!-- Module 2 -->
      <div class="module-card m2">
        <div class="module-head">
          <div class="module-num">Модуль 02 · Автоматические продажи</div>
          <span class="module-icon">🚀</span>
          <div class="module-name">VK Sales Autopilot</div>
          <div class="module-tagline">Находит клиентов, устанавливает контакт, ведёт переговоры — сам</div>
        </div>
        <div class="module-body">
          <ul class="module-features">
            <li>
              <span class="mf-icon">▶</span>
              <span>Сканирует тысячи VK-групп с вашей аудиторией каждые 15 минут — находит активных пользователей</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span>AI оценивает каждого пользователя по 10+ параметрам — до вас доходят только реально заинтересованные</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span>Пишет нативные комментарии под каждый пост — они выглядят как живое общение, а не реклама</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span>Моментально переводит в личку тех, кто ответил — пока интерес горячий, конкуренты ещё не знают о лиде</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span>Ведёт полноценный диалог по воронке продаж — rapport, интерес, квалификация, закрытие на заявку</span>
            </li>
            <li>
              <span class="mf-icon">▶</span>
              <span>Отправляет менеджеру в Telegram готового горячего лида с историей переписки и контактными данными</span>
            </li>
          </ul>
        </div>
      </div>

    </div>

    <!-- Together block -->
    <div class="together">
      <div class="together-content">
        <div class="together-icons">
          <span>🔬</span>
          <span class="t-plus">+</span>
          <span>🚀</span>
          <span class="t-eq">=</span>
          <span>💥</span>
        </div>
        <h3 class="together-title">Вместе — <span class="title-gradient">полный цикл привлечения клиентов</span></h3>
        <p class="together-desc">
          Модуль разведки находит, <strong>где живёт ваша аудитория</strong> и как с ней говорить.<br>
          Модуль продаж идёт туда и <strong>привлекает именно их</strong>.<br>
          Вы получаете готовых клиентов — без найма, без обучения, без рутины.
        </p>
        <div class="together-pills">
          <span class="t-pill">🕐 Работает пока вы спите</span>
          <span class="t-pill">📊 Вся аналитика перед глазами</span>
          <span class="t-pill">🎯 Только целевые лиды</span>
          <span class="t-pill">🔔 Уведомления о каждой конверсии</span>
          <span class="t-pill">♾️ Масштабируется без ограничений</span>
          <span class="t-pill">🔒 Ваши данные, ваша система</span>
        </div>
      </div>
    </div>

  </div>
</section>

<div class="section-divider"></div>

<!-- ════════════════════════════════════════════
     GUARANTEES
════════════════════════════════════════════ -->
<section class="guarantee-section">
  <div class="container">
    <div class="section-header">
      <span class="badge badge-gold">🛡️ Гарантии</span>
      <h2 class="section-title">Почему это<br><span class="title-gradient">надёжная инвестиция</span></h2>
    </div>

    <div class="guarantees-grid">

      <div class="g-card">
        <div class="g-icon">🔒</div>
        <div class="g-title">Ваша собственность</div>
        <div class="g-desc">Вы получаете исходный код. Система разворачивается на вашем сервере — никаких подписок, никакой зависимости</div>
      </div>

      <div class="g-card">
        <div class="g-icon">📈</div>
        <div class="g-title">Прозрачная аналитика</div>
        <div class="g-desc">Все данные — в ваших Google Sheets. Видите каждый лид, каждый диалог, каждую конверсию в режиме реального времени</div>
      </div>

      <div class="g-card">
        <div class="g-icon">⚙️</div>
        <div class="g-title">Гибкая настройка</div>
        <div class="g-desc">Меняете нишу? Меняете оффер? Переключаете параметры в одной Config-таблице — система перестраивается за минуты</div>
      </div>

      <div class="g-card">
        <div class="g-icon">🔧</div>
        <div class="g-title">Поддержка и доработки</div>
        <div class="g-desc">Система живая — обновляется, дорабатывается. Любые изменения под ваш бизнес — быстро и без бюрократии</div>
      </div>

    </div>
  </div>
</section>

<div class="section-divider"></div>

<!-- ════════════════════════════════════════════
     CTA
════════════════════════════════════════════ -->
<section class="cta-section">
  <div class="cta-bg"></div>
  <div class="container">
    <div class="cta-content">

      <span class="badge badge-green" style="margin-bottom: 24px;">🚀 Готово к внедрению</span>

      <h2 class="cta-title">
        Запустите свой<br>
        <span class="title-gradient">AI-отдел продаж сегодня</span>
      </h2>

      <p class="cta-sub">
        Пока ваши конкуренты платят зарплаты —<br>
        ваша система уже работает и приносит заявки
      </p>

      <div class="cta-box">

        <!-- Стоимость разработки -->
        <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 36px;">
          <div style="background: rgba(239,68,68,0.06); border: 1px solid rgba(239,68,68,0.2); border-radius: 16px; padding: 24px; text-align: center;">
            <div style="font-size: 11px; text-transform: uppercase; letter-spacing: 0.08em; color: var(--text3); margin-bottom: 8px;">Рыночная стоимость разработки</div>
            <div style="font-size: 36px; font-weight: 900; color: var(--red); line-height: 1; margin-bottom: 6px;">450 000 — 750 000 ₽</div>
            <div style="font-size: 12px; color: var(--text3);">проектирование + разработка + AI-промпты</div>
          </div>
          <div style="background: rgba(16,185,129,0.06); border: 1px solid rgba(16,185,129,0.25); border-radius: 16px; padding: 24px; text-align: center;">
            <div style="font-size: 11px; text-transform: uppercase; letter-spacing: 0.08em; color: var(--text3); margin-bottom: 8px;">Окупаемость</div>
            <div style="font-size: 36px; font-weight: 900; color: var(--green); line-height: 1; margin-bottom: 6px;">1.5 — 3 месяца</div>
            <div style="font-size: 12px; color: var(--text3);">за счёт отказа от рекламы и штата сотрудников</div>
          </div>
        </div>

        <div class="cta-price-label">Полная система «под ключ» включает</div>

        <div class="cta-includes">
          <div class="ci-item"><span class="ci-check">✓</span> Модуль Wordstat Intelligence (VK + Яндекс)</div>
          <div class="ci-item"><span class="ci-check">✓</span> Модуль VK Sales Autopilot</div>
          <div class="ci-item"><span class="ci-check">✓</span> SEO-оптимизация постов под алгоритмы ВК и Яндекса</div>
          <div class="ci-item"><span class="ci-check">✓</span> 12 Google Sheets таблиц аналитики</div>
          <div class="ci-item"><span class="ci-check">✓</span> AI-скоринг лидов (0–100)</div>
          <div class="ci-item"><span class="ci-check">✓</span> Полная воронка продаж в ЛС</div>
          <div class="ci-item"><span class="ci-check">✓</span> Настройка под вашу нишу и CRM</div>
          <div class="ci-item"><span class="ci-check">✓</span> Telegram-уведомления о конверсиях</div>
          <div class="ci-item"><span class="ci-check">✓</span> Исходный код — ваша собственность</div>
          <div class="ci-item"><span class="ci-check">✓</span> Техподдержка, обновление моделей</div>
        </div>

        <a href="#" class="cta-btn">
          ⚡ Записаться на демо-показ системы
        </a>

        <div class="cta-disclaimer">
          Получите расчёт окупаемости для вашего бизнеса · Разворачивается на вашем сервере · Ваши данные навсегда
        </div>
      </div>

      <!-- Final hooks -->
      <div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; margin-top: 32px;">
        <div style="background: var(--card); border: 1px solid var(--border); border-radius: 16px; padding: 24px; text-align: center;">
          <div style="font-size: 32px; margin-bottom: 8px;">⏱️</div>
          <div style="font-weight: 700; margin-bottom: 4px;">Быстрый старт</div>
          <div style="font-size: 13px; color: var(--text3);">Первые лиды — в течение суток после настройки</div>
        </div>
        <div style="background: var(--card); border: 1px solid var(--border); border-radius: 16px; padding: 24px; text-align: center;">
          <div style="font-size: 32px; margin-bottom: 8px;">💰</div>
          <div style="font-weight: 700; margin-bottom: 4px;">Окупаемость 1.5–3 месяца</div>
          <div style="font-size: 13px; color: var(--text3);">За счёт отказа от рекламного бюджета и штата — система отбивает вложения быстро</div>
        </div>
        <div style="background: var(--card); border: 1px solid var(--border); border-radius: 16px; padding: 24px; text-align: center;">
          <div style="font-size: 32px; margin-bottom: 8px;">🔒</div>
          <div style="font-weight: 700; margin-bottom: 4px;">Навсегда ваше</div>
          <div style="font-size: 13px; color: var(--text3);">Купили один раз — работает бесконечно без дополнительных платежей</div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ════════════════════════════════════════════
     FOOTER
════════════════════════════════════════════ -->
<footer>
  <div class="container">
    <div class="footer-logo">
      <img src="logo-full.jpg" alt="АТОМ">
      <div>
        <div class="footer-brand-name">АТОМ</div>
        <div class="footer-brand-sub">Алгоритмические Технологии Оптимизации Маркетинга</div>
      </div>
    </div>
    <p style="margin-bottom: 8px;"><strong>VK Lead Machine Pro</strong> — AI-система автоматической лидогенерации во ВКонтакте</p>
    <p style="margin-bottom: 16px; color: var(--text3);">Wordstat Intelligence · VK Sales Autopilot · 5 AI-процессов · 24/7</p>
    <div style="display: inline-flex; gap: 8px; flex-wrap: wrap; justify-content: center;">
      <span style="padding: 4px 14px; background: rgba(0,194,255,0.08); border: 1px solid rgba(0,194,255,0.2); border-radius: 100px; font-size: 12px; color: #67d9f7;">⚡ Интеграция ИИ в бизнес</span>
      <span style="padding: 4px 14px; background: rgba(249,115,22,0.08); border: 1px solid rgba(249,115,22,0.2); border-radius: 100px; font-size: 12px; color: #fb923c;">🎯 AI-автоматизация продаж</span>
      <span style="padding: 4px 14px; background: rgba(16,185,129,0.08); border: 1px solid rgba(16,185,129,0.2); border-radius: 100px; font-size: 12px; color: #34d399;">🔒 Ваш код — ваша система</span>
    </div>
  </div>
</footer>

<script>
  // Генерация частиц
  const container = document.getElementById('particles');
  for (let i = 0; i < 25; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    p.style.left = Math.random() * 100 + '%';
    p.style.animationDuration = (8 + Math.random() * 12) + 's';
    p.style.animationDelay = (Math.random() * 10) + 's';
    p.style.opacity = 0;
    // Разные цвета
    const colors = ['#00c2ff', '#f97316', '#7c3aed', '#00c2ff', '#f97316'];
    p.style.background = colors[Math.floor(Math.random() * colors.length)];
    p.style.width = p.style.height = (1 + Math.random() * 2) + 'px';
    container.appendChild(p);
  }

  // Плавное появление секций
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.style.opacity = '1';
        entry.target.style.transform = 'translateY(0)';
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.metric-card, .module-card, .g-card, .step-body, .pain-card').forEach(el => {
    el.style.opacity = '0';
    el.style.transform = 'translateY(20px)';
    el.style.transition = 'opacity 0.5s ease, transform 0.5s ease';
    observer.observe(el);
  });
</script>

</body>
</html>
