<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Faheem Ahmed – GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Space+Mono:wght@400;700&family=Rajdhani:wght@400;500;600;700&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #030712;
    --bg2: #0a0f1e;
    --card: #0d1526;
    --card2: #111827;
    --cyan: #00f5ff;
    --green: #00ff88;
    --purple: #a855f7;
    --pink: #ff006e;
    --yellow: #ffd600;
    --orange: #ff6b00;
    --white: #f0f6ff;
    --muted: #7a8ba0;
    --border: rgba(0,245,255,0.25);
    --glow-cyan: 0 0 20px rgba(0,245,255,0.4), 0 0 60px rgba(0,245,255,0.15);
    --glow-green: 0 0 20px rgba(0,255,136,0.4), 0 0 60px rgba(0,255,136,0.15);
    --glow-purple: 0 0 20px rgba(168,85,247,0.5), 0 0 60px rgba(168,85,247,0.2);
    --glow-pink: 0 0 20px rgba(255,0,110,0.5), 0 0 60px rgba(255,0,110,0.2);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--white);
    font-family: 'Rajdhani', sans-serif;
    overflow-x: hidden;
    line-height: 1.6;
  }

  /* ─── GRID BG ─── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,245,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,245,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 960px;
    margin: 0 auto;
    padding: 0 24px 80px;
    position: relative;
    z-index: 1;
  }

  /* ─── HERO ─── */
  .hero {
    text-align: center;
    padding: 60px 0 40px;
    position: relative;
  }

  .hero-glow {
    position: absolute;
    top: 0; left: 50%;
    transform: translateX(-50%);
    width: 600px; height: 300px;
    background: radial-gradient(ellipse, rgba(0,245,255,0.1) 0%, transparent 70%);
    pointer-events: none;
  }

  .hero h1 {
    font-family: 'Orbitron', monospace;
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 900;
    letter-spacing: 0.05em;
    background: linear-gradient(135deg, var(--cyan) 0%, var(--purple) 50%, var(--pink) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: titlePulse 3s ease-in-out infinite;
    margin-bottom: 12px;
  }

  @keyframes titlePulse {
    0%, 100% { filter: brightness(1); }
    50% { filter: brightness(1.3); }
  }

  .hero-subtitle {
    font-family: 'Space Mono', monospace;
    font-size: 0.85rem;
    color: var(--cyan);
    letter-spacing: 0.15em;
    margin-bottom: 28px;
    opacity: 0;
    animation: fadeSlideUp 0.8s 0.4s forwards;
  }

  @keyframes fadeSlideUp {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ─── TYPING LINE ─── */
  .typing-wrapper {
    background: rgba(0,245,255,0.05);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 10px 20px;
    display: inline-block;
    margin-bottom: 32px;
    font-family: 'Space Mono', monospace;
    font-size: 0.82rem;
    color: var(--green);
    overflow: hidden;
    white-space: nowrap;
  }

  .typing-text {
    display: inline-block;
    overflow: hidden;
    white-space: nowrap;
    border-right: 2px solid var(--green);
    animation: typing 4s steps(50) infinite, blink 0.7s step-end infinite;
  }

  @keyframes typing {
    0%   { width: 0; content: ''; }
    20%  { width: 100%; }
    80%  { width: 100%; }
    100% { width: 0; }
  }

  @keyframes blink {
    50% { border-color: transparent; }
  }

  /* ─── BADGE ROW ─── */
  .badge-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    margin-bottom: 36px;
    opacity: 0;
    animation: fadeSlideUp 0.8s 0.7s forwards;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 7px;
    padding: 8px 16px;
    border-radius: 50px;
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    font-weight: 700;
    letter-spacing: 0.05em;
    text-decoration: none;
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }

  .badge::before {
    content: '';
    position: absolute;
    inset: 0;
    background: rgba(255,255,255,0.05);
    opacity: 0;
    transition: opacity 0.3s;
  }

  .badge:hover::before { opacity: 1; }
  .badge:hover { transform: translateY(-3px) scale(1.05); }

  .badge-linkedin {
    background: rgba(0,119,181,0.2);
    border: 1px solid rgba(0,119,181,0.6);
    color: #4fc3f7;
    box-shadow: 0 0 12px rgba(0,119,181,0.3);
  }
  .badge-linkedin:hover { box-shadow: 0 0 24px rgba(0,119,181,0.6); }

  .badge-email {
    background: rgba(255,0,110,0.15);
    border: 1px solid rgba(255,0,110,0.5);
    color: #ff6b9d;
    box-shadow: 0 0 12px rgba(255,0,110,0.2);
  }
  .badge-email:hover { box-shadow: 0 0 24px rgba(255,0,110,0.5); }

  .badge-lms {
    background: rgba(0,251,177,0.1);
    border: 1px solid rgba(0,251,177,0.5);
    color: #00fbb1;
    box-shadow: 0 0 12px rgba(0,251,177,0.2);
  }
  .badge-lms:hover { box-shadow: 0 0 24px rgba(0,251,177,0.5); }

  .badge-github {
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.25);
    color: #e0e0e0;
    box-shadow: 0 0 12px rgba(255,255,255,0.08);
  }
  .badge-github:hover { box-shadow: 0 0 24px rgba(255,255,255,0.25); }

  /* ─── MARQUEE ─── */
  .marquee-wrapper {
    overflow: hidden;
    border-top: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    background: rgba(0,245,255,0.03);
    padding: 10px 0;
    margin-bottom: 48px;
    position: relative;
  }

  .marquee-wrapper::before,
  .marquee-wrapper::after {
    content: '';
    position: absolute;
    top: 0; bottom: 0;
    width: 80px;
    z-index: 2;
  }
  .marquee-wrapper::before { left: 0; background: linear-gradient(90deg, var(--bg), transparent); }
  .marquee-wrapper::after  { right: 0; background: linear-gradient(-90deg, var(--bg), transparent); }

  .marquee-track {
    display: flex;
    gap: 0;
    animation: marqueeScroll 30s linear infinite;
    white-space: nowrap;
    width: max-content;
  }

  .marquee-track:hover { animation-play-state: paused; }

  @keyframes marqueeScroll {
    from { transform: translateX(0); }
    to   { transform: translateX(-50%); }
  }

  .marquee-item {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 0 28px;
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    color: var(--cyan);
    letter-spacing: 0.1em;
  }

  .marquee-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--cyan);
    box-shadow: 0 0 8px var(--cyan);
    animation: dotPulse 1.5s ease-in-out infinite;
  }

  @keyframes dotPulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.6); }
  }

  /* ─── SECTION TITLES ─── */
  .section {
    margin-bottom: 48px;
    opacity: 0;
    animation: fadeSlideUp 0.7s forwards;
  }

  .section:nth-child(1) { animation-delay: 0.2s; }
  .section:nth-child(2) { animation-delay: 0.35s; }
  .section:nth-child(3) { animation-delay: 0.5s; }
  .section:nth-child(4) { animation-delay: 0.65s; }
  .section:nth-child(5) { animation-delay: 0.8s; }
  .section:nth-child(6) { animation-delay: 0.95s; }
  .section:nth-child(7) { animation-delay: 1.1s; }

  .section-title {
    font-family: 'Orbitron', monospace;
    font-size: 1.1rem;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 20px;
    display: flex;
    align-items: center;
    gap: 12px;
  }

  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  .title-cyan { color: var(--cyan); text-shadow: var(--glow-cyan); }
  .title-green { color: var(--green); text-shadow: var(--glow-green); }
  .title-purple { color: var(--purple); text-shadow: var(--glow-purple); }
  .title-pink { color: var(--pink); text-shadow: var(--glow-pink); }
  .title-yellow { color: var(--yellow); text-shadow: 0 0 20px rgba(255,214,0,0.5); }
  .title-orange { color: var(--orange); text-shadow: 0 0 20px rgba(255,107,0,0.5); }

  /* ─── CARDS ─── */
  .card {
    background: var(--card);
    border-radius: 12px;
    padding: 24px;
    border: 1px solid var(--border);
    transition: all 0.35s ease;
    position: relative;
    overflow: hidden;
  }

  .card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--cyan), var(--purple), var(--pink));
    opacity: 0;
    transition: opacity 0.35s;
  }

  .card:hover {
    border-color: rgba(0,245,255,0.5);
    box-shadow: var(--glow-cyan);
    transform: translateY(-4px);
  }

  .card:hover::before { opacity: 1; }

  /* ─── OVERVIEW CARD ─── */
  .overview-card {
    background: linear-gradient(135deg, rgba(0,245,255,0.05), rgba(168,85,247,0.05));
    border: 1px solid rgba(0,245,255,0.2);
    border-radius: 16px;
    padding: 28px 32px;
    margin-bottom: 48px;
    position: relative;
    overflow: hidden;
  }

  .overview-card::before {
    content: '';
    position: absolute;
    top: -50%; right: -20%;
    width: 300px; height: 300px;
    background: radial-gradient(circle, rgba(168,85,247,0.08), transparent 70%);
    pointer-events: none;
  }

  .overview-card p {
    font-size: 1.05rem;
    color: #c8d8e8;
    line-height: 1.8;
    margin-bottom: 14px;
  }

  .overview-card p:last-child { margin-bottom: 0; }

  .highlight { color: var(--cyan); font-weight: 600; }
  .highlight-green { color: var(--green); font-weight: 600; }
  .highlight-purple { color: var(--purple); font-weight: 600; }
  .highlight-pink { color: var(--pink); font-weight: 600; }
  .highlight-yellow { color: var(--yellow); font-weight: 600; }

  .belief-box {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background: rgba(255,214,0,0.07);
    border: 1px solid rgba(255,214,0,0.3);
    border-radius: 8px;
    padding: 10px 18px;
    margin-top: 12px;
    font-family: 'Space Mono', monospace;
    font-size: 0.82rem;
    color: var(--yellow);
    box-shadow: 0 0 16px rgba(255,214,0,0.1);
  }

  /* ─── SKILL GRID ─── */
  .skill-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
    gap: 16px;
  }

  .skill-card {
    background: var(--card2);
    border-radius: 10px;
    padding: 18px 20px;
    border: 1px solid rgba(255,255,255,0.07);
    transition: all 0.3s ease;
  }

  .skill-card:hover {
    border-color: rgba(0,245,255,0.35);
    transform: translateY(-3px);
    box-shadow: 0 8px 32px rgba(0,245,255,0.1);
  }

  .skill-card-title {
    font-family: 'Orbitron', monospace;
    font-size: 0.72rem;
    letter-spacing: 0.1em;
    color: var(--cyan);
    margin-bottom: 12px;
    display: flex;
    align-items: center;
    gap: 8px;
  }

  .skill-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;
  }

  .skill-tag {
    background: rgba(0,245,255,0.07);
    border: 1px solid rgba(0,245,255,0.2);
    border-radius: 4px;
    padding: 3px 10px;
    font-size: 0.75rem;
    color: #9ab8cc;
    font-family: 'Space Mono', monospace;
    transition: all 0.2s;
  }

  .skill-tag:hover {
    background: rgba(0,245,255,0.15);
    color: var(--cyan);
    border-color: rgba(0,245,255,0.5);
  }

  .skill-tag.green {
    background: rgba(0,255,136,0.07);
    border-color: rgba(0,255,136,0.2);
  }
  .skill-tag.green:hover {
    background: rgba(0,255,136,0.15);
    color: var(--green);
    border-color: rgba(0,255,136,0.5);
  }

  .skill-tag.purple {
    background: rgba(168,85,247,0.07);
    border-color: rgba(168,85,247,0.2);
  }
  .skill-tag.purple:hover {
    background: rgba(168,85,247,0.15);
    color: var(--purple);
    border-color: rgba(168,85,247,0.5);
  }

  /* ─── PROJECT TABLE ─── */
  .project-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.85rem;
  }

  .project-table th {
    font-family: 'Orbitron', monospace;
    font-size: 0.68rem;
    letter-spacing: 0.12em;
    color: var(--cyan);
    padding: 12px 14px;
    text-align: left;
    border-bottom: 1px solid rgba(0,245,255,0.2);
    background: rgba(0,245,255,0.04);
  }

  .project-table td {
    padding: 11px 14px;
    border-bottom: 1px solid rgba(255,255,255,0.05);
    color: #b0c4d4;
    vertical-align: top;
    transition: all 0.2s;
  }

  .project-table tr:hover td {
    background: rgba(0,245,255,0.04);
    color: var(--white);
  }

  .project-table tr:last-child td { border-bottom: none; }

  .proj-num {
    font-family: 'Space Mono', monospace;
    color: var(--muted);
    font-size: 0.75rem;
  }

  .proj-name {
    font-weight: 700;
    color: var(--white);
    font-size: 0.88rem;
  }

  .proj-tech {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: var(--green);
  }

  .proj-date {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: var(--purple);
    white-space: nowrap;
  }

  /* ─── CERT GRID ─── */
  .cert-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 14px;
  }

  .cert-card {
    background: var(--card2);
    border: 1px solid rgba(168,85,247,0.2);
    border-radius: 10px;
    padding: 16px 18px;
    transition: all 0.3s;
    position: relative;
    overflow: hidden;
  }

  .cert-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--purple), var(--pink));
    transform: scaleX(0);
    transition: transform 0.3s;
    transform-origin: left;
  }

  .cert-card:hover {
    border-color: rgba(168,85,247,0.5);
    box-shadow: var(--glow-purple);
    transform: translateY(-3px);
  }

  .cert-card:hover::after { transform: scaleX(1); }

  .cert-provider {
    font-family: 'Orbitron', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.12em;
    color: var(--purple);
    margin-bottom: 8px;
  }

  .cert-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 5px;
  }

  .cert-list li {
    font-size: 0.8rem;
    color: #9ab8cc;
    padding-left: 14px;
    position: relative;
    line-height: 1.4;
  }

  .cert-list li::before {
    content: '▸';
    position: absolute;
    left: 0;
    color: var(--purple);
    font-size: 0.65rem;
    top: 2px;
  }

  /* ─── STAT PILLS ─── */
  .stat-row {
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
    margin-bottom: 32px;
    justify-content: center;
  }

  .stat-pill {
    background: var(--card);
    border-radius: 50px;
    padding: 10px 22px;
    display: flex;
    align-items: center;
    gap: 10px;
    border: 1px solid var(--border);
    transition: all 0.3s;
  }

  .stat-pill:hover {
    box-shadow: var(--glow-cyan);
    border-color: rgba(0,245,255,0.5);
    transform: scale(1.05);
  }

  .stat-num {
    font-family: 'Orbitron', monospace;
    font-size: 1.3rem;
    font-weight: 900;
    color: var(--cyan);
  }

  .stat-label {
    font-size: 0.8rem;
    color: var(--muted);
    font-family: 'Space Mono', monospace;
  }

  /* ─── COLORFUL RAINBOW BORDER ─── */
  .rainbow-border {
    position: relative;
    border-radius: 14px;
    padding: 2px;
    background: linear-gradient(135deg, var(--cyan), var(--purple), var(--pink), var(--orange), var(--yellow), var(--green), var(--cyan));
    background-size: 300% 300%;
    animation: rainbowShift 4s ease infinite;
    margin-bottom: 48px;
  }

  @keyframes rainbowShift {
    0%   { background-position: 0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  .rainbow-inner {
    background: var(--card);
    border-radius: 13px;
    padding: 28px 32px;
  }

  /* ─── DISABILITY BADGE ─── */
  .disability-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 16px;
  }

  .dis-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(255,0,110,0.08);
    border: 1px solid rgba(255,0,110,0.35);
    border-radius: 8px;
    padding: 8px 16px;
    font-size: 0.82rem;
    font-family: 'Space Mono', monospace;
    color: #ff6b9d;
  }

  .eq-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(255,214,0,0.07);
    border: 1px solid rgba(255,214,0,0.35);
    border-radius: 8px;
    padding: 8px 16px;
    font-size: 0.82rem;
    font-family: 'Space Mono', monospace;
    color: var(--yellow);
    animation: glowPulse 2s ease-in-out infinite;
  }

  @keyframes glowPulse {
    0%, 100% { box-shadow: 0 0 8px rgba(255,214,0,0.2); }
    50% { box-shadow: 0 0 20px rgba(255,214,0,0.5); }
  }

  /* ─── FOOTER QUOTE ─── */
  .footer-quote {
    text-align: center;
    padding: 40px 20px 0;
    position: relative;
  }

  .quote-text {
    font-family: 'Space Mono', monospace;
    font-size: 1rem;
    color: var(--cyan);
    text-shadow: var(--glow-cyan);
    letter-spacing: 0.05em;
    line-height: 1.6;
    background: rgba(0,245,255,0.04);
    border: 1px solid rgba(0,245,255,0.2);
    border-radius: 10px;
    padding: 20px 32px;
    display: inline-block;
    animation: borderGlow 3s ease-in-out infinite;
  }

  @keyframes borderGlow {
    0%, 100% { border-color: rgba(0,245,255,0.2); }
    50% { border-color: rgba(0,245,255,0.6); box-shadow: var(--glow-cyan); }
  }

  /* ─── EDUCATION CARD ─── */
  .edu-grid {
    display: grid;
    gap: 14px;
  }

  .edu-card {
    background: var(--card2);
    border: 1px solid rgba(0,255,136,0.15);
    border-radius: 10px;
    padding: 16px 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 16px;
    transition: all 0.3s;
  }

  .edu-card:hover {
    border-color: rgba(0,255,136,0.4);
    box-shadow: var(--glow-green);
    transform: translateX(6px);
  }

  .edu-degree {
    font-weight: 700;
    color: var(--white);
    font-size: 0.95rem;
  }

  .edu-institution {
    font-size: 0.82rem;
    color: var(--muted);
    margin-top: 3px;
  }

  .edu-year {
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    color: var(--green);
    text-align: right;
    flex-shrink: 0;
  }

  .edu-score {
    font-family: 'Orbitron', monospace;
    font-size: 0.85rem;
    color: var(--green);
    font-weight: 700;
  }

  /* ─── IMPACT CARD ─── */
  .impact-card {
    background: linear-gradient(135deg, rgba(0,255,136,0.05), rgba(0,245,255,0.05));
    border: 1px solid rgba(0,255,136,0.2);
    border-radius: 14px;
    padding: 24px 28px;
    position: relative;
    overflow: hidden;
  }

  .impact-card::after {
    content: '';
    position: absolute;
    top: -40%; right: -10%;
    width: 200px; height: 200px;
    background: radial-gradient(circle, rgba(0,255,136,0.06), transparent);
    pointer-events: none;
  }

  .impact-point {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    padding: 10px 0;
    border-bottom: 1px solid rgba(255,255,255,0.05);
    font-size: 0.9rem;
    color: #b0c4d4;
  }

  .impact-point:last-child { border-bottom: none; }

  .impact-icon {
    font-size: 1rem;
    flex-shrink: 0;
    margin-top: 2px;
  }

  /* ─── FOCUS CARDS ─── */
  .focus-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 12px;
  }

  .focus-card {
    background: var(--card2);
    border: 1px solid rgba(255,255,255,0.07);
    border-radius: 10px;
    padding: 16px 18px;
    text-align: center;
    transition: all 0.3s;
    font-size: 0.85rem;
    color: #9ab8cc;
  }

  .focus-card:hover {
    transform: translateY(-4px);
    border-color: rgba(168,85,247,0.4);
    box-shadow: var(--glow-purple);
    color: var(--white);
  }

  .focus-icon { font-size: 1.5rem; margin-bottom: 8px; }

  /* ─── WORKSHOP ─── */
  .workshop-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
    gap: 14px;
  }

  .workshop-card {
    background: var(--card2);
    border: 1px solid rgba(255,107,0,0.2);
    border-radius: 10px;
    padding: 18px 20px;
    transition: all 0.3s;
  }

  .workshop-card:hover {
    border-color: rgba(255,107,0,0.5);
    box-shadow: 0 0 20px rgba(255,107,0,0.2);
    transform: translateY(-3px);
  }

  .workshop-title {
    font-weight: 700;
    color: var(--orange);
    font-size: 0.9rem;
    margin-bottom: 6px;
  }

  .workshop-meta {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    color: var(--muted);
  }

  /* ─── SCROLLBAR ─── */
  ::-webkit-scrollbar { width: 6px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: rgba(0,245,255,0.3); border-radius: 3px; }
  ::-webkit-scrollbar-thumb:hover { background: rgba(0,245,255,0.6); }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 600px) {
    .project-table { font-size: 0.75rem; }
    .project-table td, .project-table th { padding: 8px 8px; }
    .hero h1 { font-size: 1.6rem; }
    .rainbow-inner { padding: 20px 16px; }
  }
</style>
</head>
<body>

<div class="container">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-glow"></div>
    <h1>FAHEEM AHMED</h1>
    <p class="hero-subtitle">FRONTEND-FOCUSED FULL STACK DEVELOPER &nbsp;|&nbsp; EDTECH ENTREPRENEUR &nbsp;|&nbsp; FOUNDER – SKILLVERSE TECHNOLOGIES</p>

    <div class="typing-wrapper">
      <span class="typing-text" id="typer"></span>
    </div>

    <div class="badge-row">
      <a href="https://www.linkedin.com/in/ahmed-faheem-07b053349" target="_blank" class="badge badge-linkedin">
        🔗 LinkedIn — Professional
      </a>
      <a href="mailto:masfmohammed027@gmail.com" class="badge badge-email">
        ✉️ masfmohammed027@gmail.com
      </a>
      <a href="https://skillversetechnologies.talentlms.com" target="_blank" class="badge badge-lms">
        🎓 SkillVerse LMS
      </a>
      <a href="https://github.com" target="_blank" class="badge badge-github">
        💻 GitHub
      </a>
    </div>
  </div>

  <!-- MARQUEE -->
  <div class="marquee-wrapper">
    <div class="marquee-track" id="marqueeTrack">
      <!-- JS duplicates for infinite scroll -->
    </div>
  </div>

  <!-- STAT PILLS -->
  <div class="stat-row">
    <div class="stat-pill">
      <span class="stat-num">17</span>
      <span class="stat-label">PROJECTS</span>
    </div>
    <div class="stat-pill">
      <span class="stat-num">32</span>
      <span class="stat-label">CERTIFICATIONS</span>
    </div>
    <div class="stat-pill">
      <span class="stat-num">5</span>
      <span class="stat-label">PLATFORMS</span>
    </div>
    <div class="stat-pill">
      <span class="stat-num">4</span>
      <span class="stat-label">LANGUAGES</span>
    </div>
  </div>

  <!-- OVERVIEW -->
  <div class="rainbow-border">
    <div class="rainbow-inner">
      <p>
        I am a <span class="highlight">Computer Science Diploma student and software developer</span> with hands-on experience building <span class="highlight">production-ready web applications</span> using React 19, JavaScript (ES6+), Spring Boot, and Python.
        I have built and deployed <span class="highlight-green">17 real-world projects</span> spanning frontend systems, backend APIs, Progressive Web Applications, and AI prototypes.
      </p>
      <p>
        I am the <span class="highlight-purple">Founder of SkillVerse Technologies</span>, a non-profit inclusive learning initiative built on Universal Design principles — making technology education accessible, practical, and beginner-friendly, especially for <span class="highlight-pink">differently-abled learners</span>.
      </p>
      <div class="disability-row">
        <span class="dis-badge">♿ Locomotor Disability (Cerebral Palsy – 75%)</span>
        <span class="eq-badge">💡 Technology is the Universal Equalizer</span>
      </div>
    </div>
  </div>

  <!-- EDUCATION -->
  <div class="section">
    <div class="section-title title-green">🎓 Education</div>
    <div class="edu-grid">
      <div class="edu-card">
        <div>
          <div class="edu-degree">Diploma in Computer Science & Engineering</div>
          <div class="edu-institution">JSS Polytechnic for the Differently Abled, Mysuru</div>
        </div>
        <div class="edu-year">2023 – 2026<br/><span class="edu-score">In Progress</span></div>
      </div>
      <div class="edu-card">
        <div>
          <div class="edu-degree">Pre-University Course (EBAC)</div>
          <div class="edu-institution">SVG Vishwaprajna Composite PU College</div>
        </div>
        <div class="edu-year">2022<br/><span class="edu-score">86%</span></div>
      </div>
      <div class="edu-card">
        <div>
          <div class="edu-degree">SSLC</div>
          <div class="edu-institution">Vishwamanava Vidyanikethana</div>
        </div>
        <div class="edu-year">2019<br/><span class="edu-score">88%</span></div>
      </div>
    </div>
  </div>

  <!-- SKILLVERSE -->
  <div class="section">
    <div class="section-title title-cyan">🚀 Entrepreneurship &amp; Social Impact</div>
    <div class="impact-card">
      <div class="impact-point">
        <span class="impact-icon">🏗️</span>
        <span>Founded and manage <span class="highlight">SkillVerse Technologies</span> — an inclusive online learning platform built on TalentLMS, delivering structured digital education to beginner learners.</span>
      </div>
      <div class="impact-point">
        <span class="impact-icon">📐</span>
        <span>Designed structured courses, LMS workflows, learner onboarding, and content delivery with a focus on <span class="highlight-green">Universal Design principles</span>.</span>
      </div>
      <div class="impact-point">
        <span class="impact-icon">🎥</span>
        <span>Running a <span class="highlight-purple">YouTube channel</span> providing digital skill tutorials for beginners and homemakers under the Skillverse Technologies brand.</span>
      </div>
      <div class="impact-point">
        <span class="impact-icon">🔗</span>
        <span>Platform: <a href="https://skillversetechnologies.talentlms.com" target="_blank" style="color:var(--cyan);text-decoration:none;">skillversetechnologies.talentlms.com</a></span>
      </div>
    </div>
  </div>

  <!-- WORKSHOPS -->
  <div class="section">
    <div class="section-title title-orange">🧪 Workshops &amp; Innovation</div>
    <div class="workshop-grid">
      <div class="workshop-card">
        <div class="workshop-title">🤖 Hackathon on Assistive Technology</div>
        <div class="workshop-meta">AIISH, Mysuru &nbsp;|&nbsp; 2025<br/>Innovation event focused on inclusive technology solutions</div>
      </div>
      <div class="workshop-card">
        <div class="workshop-title">💼 Career Awareness Workshop (2 Days)</div>
        <div class="workshop-meta">EnAble India &amp; JSS PDA &nbsp;|&nbsp; Sept 26–27, 2025<br/>Professional development &amp; career readiness program</div>
      </div>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="section">
    <div class="section-title title-cyan">🛠️ Technical Skill Set</div>
    <div class="skill-grid">
      <div class="skill-card">
        <div class="skill-card-title">⚛️ Frontend Engineering</div>
        <div class="skill-tags">
          <span class="skill-tag">React 19</span>
          <span class="skill-tag">React Router 6</span>
          <span class="skill-tag">Hooks</span>
          <span class="skill-tag">Context API</span>
          <span class="skill-tag">PWA</span>
          <span class="skill-tag">Service Workers</span>
          <span class="skill-tag">JavaScript ES6+</span>
          <span class="skill-tag">HTML5</span>
          <span class="skill-tag">CSS3</span>
          <span class="skill-tag">GSAP</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-title" style="color:var(--green);">⚙️ Backend Development</div>
        <div class="skill-tags">
          <span class="skill-tag green">Java</span>
          <span class="skill-tag green">Spring Boot</span>
          <span class="skill-tag green">REST APIs</span>
          <span class="skill-tag green">CRUD Systems</span>
          <span class="skill-tag green">Layered Architecture</span>
          <span class="skill-tag green">Validation</span>
          <span class="skill-tag green">Exception Handling</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-title" style="color:var(--yellow);">🗄️ Databases</div>
        <div class="skill-tags">
          <span class="skill-tag">MySQL</span>
          <span class="skill-tag">MongoDB</span>
          <span class="skill-tag">Data Modeling</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-title" style="color:var(--orange);">☁️ DevOps &amp; Cloud</div>
        <div class="skill-tags">
          <span class="skill-tag">Linux Admin</span>
          <span class="skill-tag">Kubernetes</span>
          <span class="skill-tag">Git / GitHub</span>
          <span class="skill-tag">Postman</span>
          <span class="skill-tag">Vercel</span>
          <span class="skill-tag">Netlify</span>
          <span class="skill-tag">DevOps & SRE</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-title" style="color:var(--purple);">🤖 AI &amp; Analytics</div>
        <div class="skill-tags">
          <span class="skill-tag purple">Python</span>
          <span class="skill-tag purple">NLP (TextBlob)</span>
          <span class="skill-tag purple">Prompt Engineering</span>
          <span class="skill-tag purple">Power BI</span>
          <span class="skill-tag purple">Tableau</span>
          <span class="skill-tag purple">Big Data Analytics</span>
        </div>
      </div>
      <div class="skill-card">
        <div class="skill-card-title" style="color:var(--pink);">🔐 Specialized</div>
        <div class="skill-tags">
          <span class="skill-tag">Info Security</span>
          <span class="skill-tag">Blockchain</span>
          <span class="skill-tag">Accessibility Design</span>
          <span class="skill-tag">Cybersecurity</span>
          <span class="skill-tag">Kali Linux</span>
          <span class="skill-tag">Cryptography</span>
        </div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section">
    <div class="section-title title-yellow">📦 Project Portfolio — 17 Real-World Projects</div>
    <div class="card">
      <table class="project-table">
        <thead>
          <tr>
            <th>#</th>
            <th>Project</th>
            <th>Tech Stack</th>
            <th>Date</th>
          </tr>
        </thead>
        <tbody>
          <tr><td class="proj-num">01</td><td class="proj-name">Holy Quran Mushaf App</td><td class="proj-tech">HTML5, CSS3, JS, PWA</td><td class="proj-date">Feb 19, 2026</td></tr>
          <tr><td class="proj-num">02</td><td class="proj-name">Stream Nest</td><td class="proj-tech">React 19, Router 6, Context API</td><td class="proj-date">Feb 11, 2026</td></tr>
          <tr><td class="proj-num">03</td><td class="proj-name">Admin Dashboard</td><td class="proj-tech">React, JavaScript, CSS</td><td class="proj-date">Feb 4, 2026</td></tr>
          <tr><td class="proj-num">04</td><td class="proj-name">Random Quotes Generator</td><td class="proj-tech">HTML5, CSS3, JS</td><td class="proj-date">Jan 30, 2026</td></tr>
          <tr><td class="proj-num">05</td><td class="proj-name">FoodLand</td><td class="proj-tech">React.js, JSX, CSS</td><td class="proj-date">Jan 27, 2026</td></tr>
          <tr><td class="proj-num">06</td><td class="proj-name">Breezl Weather Web App</td><td class="proj-tech">JS, GSAP, Fetch API</td><td class="proj-date">Jan 22, 2026</td></tr>
          <tr><td class="proj-num">07</td><td class="proj-name">React Counter App</td><td class="proj-tech">React, Hooks, LocalStorage</td><td class="proj-date">Jan 19, 2026</td></tr>
          <tr><td class="proj-num">08</td><td class="proj-name">Faheem's Reel Explorer</td><td class="proj-tech">React, OMDb API</td><td class="proj-date">Jan 15, 2026</td></tr>
          <tr><td class="proj-num">09</td><td class="proj-name">Flowly Landing Page</td><td class="proj-tech">HTML5, CSS3, GSAP, SVG</td><td class="proj-date">Jan 13, 2026</td></tr>
          <tr><td class="proj-num">10</td><td class="proj-name">Vanilla JS To-Do List</td><td class="proj-tech">Vanilla JS, LocalStorage</td><td class="proj-date">Jan 12, 2026</td></tr>
          <tr><td class="proj-num">11</td><td class="proj-name">Smart Calculator (V2)</td><td class="proj-tech">HTML5, CSS3, JS</td><td class="proj-date">—</td></tr>
          <tr><td class="proj-num">12</td><td class="proj-name">Islamic Quiz App</td><td class="proj-tech">HTML5, CSS3, JS</td><td class="proj-date">—</td></tr>
          <tr><td class="proj-num">13</td><td class="proj-name">Student Marks Manager</td><td class="proj-tech">React.js, Vercel</td><td class="proj-date">—</td></tr>
          <tr><td class="proj-num">14</td><td class="proj-name">Mario-style 2D Game</td><td class="proj-tech">React.js, Game Logic</td><td class="proj-date">—</td></tr>
          <tr><td class="proj-num">15</td><td class="proj-name">Todo React App</td><td class="proj-tech">React.js, Hooks</td><td class="proj-date">—</td></tr>
          <tr><td class="proj-num">16</td><td class="proj-name">Spring Boot CRUD Systems</td><td class="proj-tech">Java, Spring Boot, MySQL, MongoDB</td><td class="proj-date">2025</td></tr>
          <tr><td class="proj-num">17</td><td class="proj-name">Zikra – AI Assistant</td><td class="proj-tech">Python, NLP (TextBlob)</td><td class="proj-date">2025</td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <!-- CERTIFICATIONS -->
  <div class="section">
    <div class="section-title title-purple">📜 Certifications — 32 Verified</div>
    <div class="cert-grid">
      <div class="cert-card">
        <div class="cert-provider">🐧 THE LINUX FOUNDATION</div>
        <ul class="cert-list">
          <li>Introduction to Linux (LFS101)</li>
          <li>Introduction to Kubernetes (LFS158)</li>
          <li>Open Source Software Dev (LFD102)</li>
          <li>DevOps & SRE Fundamentals (LFS162)</li>
        </ul>
      </div>
      <div class="cert-card">
        <div class="cert-provider">🔵 IBM SKILLSBUILD</div>
        <ul class="cert-list">
          <li>Data Fundamentals</li>
          <li>Introduction to React</li>
          <li>JavaScript Tutorial</li>
          <li>Web App Fundamentals</li>
        </ul>
      </div>
      <div class="cert-card">
        <div class="cert-provider">🟠 INFOSYS SPRINGBOARD</div>
        <ul class="cert-list">
          <li>Learning React</li>
          <li>Webpack for React Applications</li>
          <li>HTML5 with JS & CSS3</li>
          <li>Java Features</li>
          <li>Information Security Fundamentals</li>
        </ul>
      </div>
      <div class="cert-card">
        <div class="cert-provider">🟢 SIMPLILEARN</div>
        <ul class="cert-list">
          <li>Full Stack Java Development</li>
          <li>Artificial Intelligence</li>
          <li>Blockchain Developer Training</li>
          <li>Cyber Security & ChatGPT for Cyber</li>
          <li>Kali Linux & Cryptography</li>
          <li>Power BI & Tableau</li>
          <li>Big Data Tools & Excel Automation</li>
        </ul>
      </div>
      <div class="cert-card">
        <div class="cert-provider">🌐 FUTURESKILLS PRIME</div>
        <ul class="cert-list">
          <li>Cloud Computing Applications (Mar 3, 2026)</li>
          <li>Prompt Engineering (Feb 23, 2026)</li>
          <li>Big Data Analytics (Feb 20, 2026)</li>
        </ul>
      </div>
      <div class="cert-card">
        <div class="cert-provider">🏆 LEADERSHIP & PROFESSIONAL DEV</div>
        <ul class="cert-list">
          <li>Project Management 101</li>
          <li>Time Management</li>
          <li>Career Awareness — EnAble India</li>
          <li>Physical Activity Audit</li>
          <li>Assistive Tech Hackathon — AIISH</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- CURRENT FOCUS -->
  <div class="section">
    <div class="section-title title-pink">🎯 Current Focus</div>
    <div class="focus-grid">
      <div class="focus-card">
        <div class="focus-icon">⚛️</div>
        Industry-ready Frontend & Full-Stack Development
      </div>
      <div class="focus-card">
        <div class="focus-icon">🏗️</div>
        Advanced Backend System Design — Spring Boot
      </div>
      <div class="focus-card">
        <div class="focus-icon">♿</div>
        Accessible & Scalable Software
      </div>
      <div class="focus-card">
        <div class="focus-icon">🎓</div>
        SkillVerse Technologies Growth
      </div>
      <div class="focus-card">
        <div class="focus-icon">🌍</div>
        Open-Source Contribution
      </div>
    </div>
  </div>

  <!-- FOOTER QUOTE -->
  <div class="footer-quote">
    <div class="quote-text">
      "I don't just learn technology — I build systems that work in the real world."<br/>
      <span style="font-size:0.72rem;color:var(--muted);margin-top:8px;display:block;">— Faheem Ahmed &nbsp;|&nbsp; Mysuru, Karnataka, India</span>
    </div>
  </div>

</div><!-- /container -->

<script>
  // ─── TYPING ANIMATION ───
  const lines = [
    "Computer Science Diploma Student",
    "Frontend-Focused Full Stack Developer",
    "React 19 | Spring Boot | Java | Python",
    "17 Real-World Projects | 32 Certifications",
    "Founder — SkillVerse Technologies",
    "Building Accessible & Scalable Software",
  ];

  let lineIdx = 0, charIdx = 0, deleting = false;
  const typer = document.getElementById('typer');

  function type() {
    const current = lines[lineIdx];
    if (!deleting) {
      charIdx++;
      typer.textContent = current.slice(0, charIdx);
      if (charIdx === current.length) {
        deleting = true;
        setTimeout(type, 1800);
        return;
      }
    } else {
      charIdx--;
      typer.textContent = current.slice(0, charIdx);
      if (charIdx === 0) {
        deleting = false;
        lineIdx = (lineIdx + 1) % lines.length;
      }
    }
    setTimeout(type, deleting ? 40 : 70);
  }
  type();

  // ─── MARQUEE BUILD ───
  const marqueeItems = [
    "React 19", "Spring Boot", "Java", "Python", "PWA",
    "REST APIs", "MySQL", "MongoDB", "Kubernetes",
    "Linux", "GSAP", "JavaScript ES6+", "17 Projects",
    "32 Certifications", "SkillVerse Technologies",
    "Frontend Developer", "Full Stack Developer",
    "Accessibility-First", "EdTech Entrepreneur",
    "Prompt Engineering", "Big Data Analytics",
    "Netlify", "Vercel", "Git & GitHub",
  ];

  const track = document.getElementById('marqueeTrack');
  // Duplicate for seamless scroll
  [...marqueeItems, ...marqueeItems].forEach(item => {
    const el = document.createElement('span');
    el.className = 'marquee-item';
    el.innerHTML = `<span class="marquee-dot"></span>${item}`;
    track.appendChild(el);
  });
</script>
</body>
</html>
