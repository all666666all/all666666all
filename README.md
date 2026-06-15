<!-- @dsCard group="GitHub Profile" viewport="860x720" name="GitHub Profile" subtitle="Light/dark toggle · typing animation · skillicons · stats" -->
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chengzong</title>
<link rel="stylesheet" href="../../styles.css">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html, body {
    min-height: 100vh;
    font-family: var(--font-sans);
    background: var(--color-bg-primary);
    color: var(--color-fg-primary);
    transition: background-color var(--duration-normal) var(--ease-default),
                color var(--duration-normal) var(--ease-default);
  }

  /* ── Top bar ───────────────────────────────────────── */
  .topbar {
    position: sticky; top: 0; z-index: 10;
    height: 52px;
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 32px;
    background: color-mix(in srgb, var(--color-bg-primary) 80%, transparent);
    border-bottom: var(--border-subtle);
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
  }

  .topbar-left { display: flex; align-items: center; gap: 10px; }

  .gh-logo { width: 24px; height: 24px; fill: var(--color-fg-primary); flex-shrink: 0; }

  .topbar-user {
    font-size: var(--text-sm);
    font-weight: var(--font-medium);
    color: var(--color-fg-secondary);
    letter-spacing: var(--tracking-normal);
  }

  .theme-btn {
    width: 32px; height: 32px;
    border-radius: var(--radius-full);
    border: var(--border-default);
    background: var(--color-bg-secondary);
    color: var(--color-fg-tertiary);
    cursor: pointer; display: flex; align-items: center; justify-content: center;
    font-size: 14px; line-height: 1;
    transition: background-color var(--duration-fast) var(--ease-default);
  }
  .theme-btn:hover { background: var(--color-bg-tertiary); }

  /* ── Main content ──────────────────────────────────── */
  .main {
    max-width: 680px;
    margin: 0 auto;
    padding: 56px 24px 80px;
    text-align: center;
  }

  /* ── Avatar ────────────────────────────────────────── */
  .avatar {
    width: 88px; height: 88px;
    border-radius: 50%;
    border: var(--border-default);
    object-fit: cover;
    display: block;
    margin: 0 auto 24px;
    background: var(--color-bg-secondary);
  }

  /* ── Identity ──────────────────────────────────────── */
  .name {
    font-size: var(--text-5xl);
    font-weight: var(--font-semibold);
    letter-spacing: var(--tracking-tightest);
    line-height: 1;
    color: var(--color-fg-primary);
    margin-bottom: 12px;
  }

  .subtitle {
    font-size: var(--text-base);
    color: var(--color-fg-tertiary);
    letter-spacing: 0.03em;
    margin-bottom: 20px;
  }

  /* ── Typing ────────────────────────────────────────── */
  .typing-wrap {
    height: 32px;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 44px;
    gap: 2px;
  }

  .typing-text {
    font-size: var(--text-base);
    color: var(--color-fg-tertiary);
    font-weight: var(--font-regular);
  }

  .cursor {
    display: inline-block;
    width: 2px; height: 1em;
    background: var(--color-accent);
    vertical-align: middle;
    animation: blink 1s step-end infinite;
    border-radius: 1px;
    flex-shrink: 0;
  }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  /* ── Divider ───────────────────────────────────────── */
  .divider { border: none; border-top: var(--border-subtle); margin: 0 0 40px; }

  /* ── Sections ──────────────────────────────────────── */
  .section { text-align: left; margin-bottom: 44px; }

  .section-heading {
    font-size: var(--text-lg);
    font-weight: var(--font-semibold);
    color: var(--color-fg-primary);
    margin-bottom: 16px;
    letter-spacing: var(--tracking-snug);
  }

  /* ── About ─────────────────────────────────────────── */
  .about-body {
    font-size: var(--text-md);
    color: var(--color-fg-secondary);
    line-height: var(--leading-relaxed);
    text-wrap: pretty;
  }

  .about-aside {
    font-size: var(--text-sm);
    color: var(--color-fg-tertiary);
    margin-top: 14px;
    letter-spacing: 0.01em;
  }

  /* ── Toolbox ───────────────────────────────────────── */
  .icon-img { display: block; height: 42px; }

  /* ── Stats ─────────────────────────────────────────── */
  .stats-row {
    display: flex; gap: 16px; flex-wrap: wrap; align-items: flex-start;
  }
  .stats-row img { border-radius: var(--radius-md); height: 155px; max-width: 100%; }

  /* ── Quote ─────────────────────────────────────────── */
  .quote {
    font-size: var(--text-sm);
    color: var(--color-fg-quaternary);
    text-align: center;
    letter-spacing: 0.03em;
  }
</style>
</head>
<body>

  <nav class="topbar">
    <div class="topbar-left">
      <svg class="gh-logo" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
      </svg>
      <span class="topbar-user">all666666all</span>
    </div>
    <button class="theme-btn" id="themeBtn" aria-label="Toggle theme">☀</button>
  </nav>

  <main class="main">

    <img
      class="avatar"
      src="https://github.com/all666666all.png"
      alt="Chengzong avatar"
    />

    <h1 class="name">Chengzong</h1>
    <p class="subtitle">Computational&nbsp;Biology&nbsp;·&nbsp;Data&nbsp;Science</p>

    <div class="typing-wrap">
      <span class="typing-text" id="typingEl"></span>
      <span class="cursor"></span>
    </div>

    <hr class="divider" />

    <section class="section">
      <h2 class="section-heading">About</h2>
      <p class="about-body">
        I come from the life sciences, now moving toward <strong>AI &amp; data</strong>.<br>
        I work where biology meets machine learning —<br>
        turning experiments into datasets, and datasets into understanding.
      </p>
      <p class="about-aside">来自生命科学，正走向 AI 与数据 · 安静地构建，持续地学习</p>
    </section>

    <section class="section">
      <h2 class="section-heading">Toolbox</h2>
      <img
        class="icon-img"
        src="https://skillicons.dev/icons?i=python,r,pytorch,tensorflow,sklearn,anaconda,docker,git,linux,vscode&perline=10"
        alt="Python, R, PyTorch, TensorFlow, scikit-learn, Anaconda, Docker, Git, Linux, VSCode"
      />
    </section>

    <section class="section">
      <h2 class="section-heading">GitHub</h2>
      <div class="stats-row">
        <img id="statsImg" alt="GitHub stats" />
        <img id="langsImg" alt="Top languages" />
      </div>
    </section>

    <p class="quote">「 Let the data tell the story of life. 」</p>

  </main>

  <script>
    // ── Typing animation ──────────────────────────────
    const LINES = ['Biology → AI / Data', '用数据解读生命'];
    let li = 0, ci = 0, del = false;
    const el = document.getElementById('typingEl');

    function tick() {
      const word = LINES[li];
      if (!del) {
        el.textContent = word.slice(0, ++ci);
        if (ci === word.length) { del = true; setTimeout(tick, 2400); return; }
        setTimeout(tick, 85);
      } else {
        el.textContent = word.slice(0, --ci);
        if (ci === 0) { del = false; li = (li + 1) % LINES.length; setTimeout(tick, 500); return; }
        setTimeout(tick, 42);
      }
    }
    tick();

    // ── Theme toggle ─────────────────────────────────
    const btn = document.getElementById('themeBtn');
    const statsImg = document.getElementById('statsImg');
    const langsImg = document.getElementById('langsImg');

    // Detect system preference
    let dark = window.matchMedia('(prefers-color-scheme: dark)').matches;

    function applyTheme() {
      document.documentElement.setAttribute('data-theme', dark ? 'dark' : '');
      btn.textContent = dark ? '☾' : '☀';

      const tc = dark ? 'f5f5f7' : '1d1d1f';
      const sc = dark ? '86868b' : '515154';
      const ic = dark ? '2997ff' : '0071e3';
      const bg = '00000000';

      statsImg.src = `https://github-readme-stats.vercel.app/api?username=all666666all&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&title_color=${tc}&text_color=${sc}&icon_color=${ic}&bg_color=${bg}`;
      langsImg.src = `https://github-readme-stats.vercel.app/api/top-langs/?username=all666666all&layout=compact&hide_border=true&langs_count=6&title_color=${tc}&text_color=${sc}&bg_color=${bg}`;
    }

    applyTheme();
    btn.addEventListener('click', () => { dark = !dark; applyTheme(); });
  </script>

</body>
</html>
