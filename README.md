<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday, Gladys 🌹</title>
<link href="https://fonts.googleapis.com/css2?family=IM+Fell+English:ital@0;1&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400;1,500&family=Cinzel+Decorative:wght@400&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --deep: #03010a;
    --dark: #0a0318;
    --mid: #150a2e;
    --purple: #2d1060;
    --violet: #4a1a8a;
    --lavender: #7b3fc4;
    --lilac: #b07ee8;
    --mist: #d4b8f0;
    --silver: #e8e0f5;
    --gold: #c9a96e;
    --rose: #e8a0b8;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Cormorant Garamond', 'Times New Roman', serif;
    background: var(--deep);
    color: var(--silver);
    overflow-x: hidden;
  }

  /* ─── PARTICLES CANVAS ─── */
  #particles {
    position: fixed;
    top: 0; left: 0;
    width: 100%; height: 100%;
    pointer-events: none;
    z-index: 0;
  }

  /* ─── SECTION BASE ─── */
  section {
    position: relative;
    z-index: 1;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 60px 40px;
  }

  /* ─── SECTION 1: HERO ─── */
  #hero {
    background: radial-gradient(ellipse at 50% 30%, #1e0745 0%, #0a0220 40%, var(--deep) 75%);
    text-align: center;
  }

  .subtitle-tag {
    font-family: 'Cormorant Garamond', serif;
    font-size: 0.78rem;
    font-weight: 400;
    letter-spacing: 0.35em;
    color: var(--lilac);
    text-transform: uppercase;
    margin-bottom: 2.5rem;
    opacity: 0;
    animation: fadeUp 1s ease 0.3s forwards;
    display: flex;
    align-items: center;
    gap: 14px;
  }
  .subtitle-tag::before,
  .subtitle-tag::after {
    content: '';
    width: 40px;
    height: 0.5px;
    background: var(--lavender);
    opacity: 0.6;
  }

  .hero-happy {
    font-family: 'IM Fell English', 'Times New Roman', serif;
    font-style: italic;
    font-size: clamp(5rem, 14vw, 10rem);
    font-weight: 400;
    color: var(--mist);
    line-height: 0.9;
    opacity: 0;
    animation: fadeUp 1.2s ease 0.6s forwards;
    text-shadow: 0 0 80px rgba(176, 126, 232, 0.25);
    letter-spacing: -0.01em;
  }

  .hero-birthday {
    font-family: 'Cinzel Decorative', 'Times New Roman', serif;
    font-size: clamp(2.2rem, 7vw, 5.5rem);
    font-weight: 400;
    letter-spacing: 0.18em;
    color: var(--silver);
    line-height: 1.1;
    opacity: 0;
    animation: fadeUp 1.2s ease 0.9s forwards;
    text-shadow: 0 0 60px rgba(120, 60, 200, 0.4);
    margin-top: 0.1em;
    text-transform: uppercase;
  }

  .hero-mylove {
    font-family: 'Cormorant Garamond', serif;
    font-style: italic;
    font-size: clamp(1.1rem, 3vw, 1.6rem);
    font-weight: 300;
    letter-spacing: 0.4em;
    color: var(--lilac);
    text-transform: uppercase;
    margin-top: 2rem;
    opacity: 0;
    animation: fadeUp 1s ease 1.2s forwards;
  }

  .hero-divider {
    width: 120px;
    height: 0.5px;
    background: linear-gradient(90deg, transparent, var(--lavender), transparent);
    margin: 2rem auto;
    opacity: 0;
    animation: fadeIn 1s ease 1.5s forwards;
  }

  .hero-dot {
    width: 6px; height: 6px;
    background: var(--lavender);
    border-radius: 50%;
    margin: 0 auto 1.5rem;
    opacity: 0;
    animation: fadeIn 1s ease 1.6s forwards;
  }

  .hero-date {
    font-family: 'Cormorant Garamond', serif;
    font-size: 0.78rem;
    font-weight: 400;
    letter-spacing: 0.4em;
    color: var(--mist);
    text-transform: uppercase;
    opacity: 0;
    animation: fadeUp 1s ease 1.7s forwards;
  }
  .hero-date span { color: var(--lilac); }

  .hero-tagline {
    font-family: 'IM Fell English', serif;
    font-style: italic;
    font-size: clamp(0.95rem, 2.2vw, 1.25rem);
    font-weight: 400;
    color: rgba(212, 184, 240, 0.7);
    margin-top: 0.8rem;
    opacity: 0;
    animation: fadeUp 1s ease 1.9s forwards;
  }

  .scroll-hint {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    opacity: 0;
    animation: fadeIn 1s ease
