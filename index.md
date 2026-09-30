<style>
  :root {
    --text: #1f2933;
    --muted: #52616f;
    --line: #d9e2ec;
    --surface: #f7f9fb;
    --accent: #235789;
    --accent-dark: #173f5f;
  }

  body {
    color: var(--text);
    background: linear-gradient(180deg, #ffffff 0%, #f6f8fb 100%);
  }

  .home {
    max-width: 980px;
    margin: 0 auto;
    padding: 32px 20px 56px;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    line-height: 1.65;
  }

  .hero {
    display: grid;
    grid-template-columns: minmax(0, 1fr) 240px;
    gap: 40px;
    align-items: center;
    padding: 28px 0 34px;
    border-bottom: 1px solid var(--line);
  }

  .eyebrow {
    margin: 0 0 8px;
    color: var(--accent);
    font-size: 0.82rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .hero h1 {
    margin: 0;
    color: #102a43;
    font-size: clamp(2.25rem, 5vw, 3.6rem);
    font-weight: 750;
    line-height: 1.05;
  }

  .subtitle {
    margin: 16px 0 0;
    color: var(--muted);
    font-size: 1.08rem;
    max-width: 650px;
  }

  .interests {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin: 22px 0 0;
    padding: 0;
    list-style: none;
  }

  .interests li {
    padding: 5px 10px;
    border: 1px solid #c7d8ea;
    border-radius: 999px;
    color: var(--accent-dark);
    background: #f2f7fc;
    font-size: 0.88rem;
    font-weight: 600;
  }

  .portrait-wrap {
    justify-self: end;
    width: min(240px, 42vw);
  }

  .portrait {
    display: block;
    width: 100%;
    aspect-ratio: 1 / 1.12;
    object-fit: cover;
    object-position: center 18%;
    border: 1px solid #c8d2dc;
    border-radius: 10px;
    box-shadow: 0 16px 38px rgba(16, 42, 67, 0.16);
    background: #ffffff;
  }

  .content-section {
    padding: 30px 0;
    border-bottom: 1px solid var(--line);
  }

  .content-section:last-child {
    border-bottom: 0;
  }

  .section-heading {
    margin: 0 0 18px;
    color: #102a43;
    font-size: 1.45rem;
    line-height: 1.25;
  }

  .papers {
    display: grid;
    gap: 12px;
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .papers li {
    padding: 14px 16px;
    border-left: 3px solid var(--accent);
    background: rgba(255, 255, 255, 0.78);
    box-shadow: 0 1px 0 rgba(16, 42, 67, 0.08);
  }

  a {
    color: var(--accent);
    text-decoration-thickness: 1px;
    text-underline-offset: 3px;
  }

  a:hover {
    color: var(--accent-dark);
  }

  .link-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 12px;
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .link-grid a {
    display: block;
    min-height: 100%;
    padding: 13px 15px;
    border: 1px solid var(--line);
    border-radius: 8px;
    background: #ffffff;
    color: #1f4e79;
    font-weight: 650;
    text-decoration: none;
    box-shadow: 0 1px 2px rgba(16, 42, 67, 0.05);
    transition: border-color 160ms ease, box-shadow 160ms ease, transform 160ms ease;
  }

  .link-grid a:hover {
    border-color: #9fb9d3;
    box-shadow: 0 8px 20px rgba(16, 42, 67, 0.09);
    transform: translateY(-1px);
  }

  @media (max-width: 720px) {
    .home {
      padding: 24px 16px 42px;
    }

    .hero {
      grid-template-columns: 1fr;
      gap: 24px;
      padding-top: 16px;
    }

    .portrait-wrap {
      justify-self: start;
      width: min(210px, 62vw);
      order: -1;
    }

    .link-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<main class="home">
  <section class="hero">
    <div>
      <p class="eyebrow">Computer Science · Artificial Intelligence</p>
      <h1>Zheng Luo</h1>
      <p class="subtitle">
        Master's student at USC working on large language models, agentic systems,
        reinforcement learning, and explicit, explainable AI.
      </p>
      <ul class="interests" aria-label="Research interests">
        <li>LLM</li>
        <li>Agentic Systems</li>
        <li>Reinforcement Learning</li>
        <li>Rule-Based AI</li>
        <li>Explainable AI</li>
      </ul>
    </div>
    <div class="portrait-wrap">
      <img class="portrait" src="zheng_luo.jpg" alt="Portrait of Zheng Luo">
    </div>
  </section>

  <section class="content-section" aria-labelledby="papers-heading">
    <h2 id="papers-heading" class="section-heading">Papers Published or Under Review</h2>
    <ul class="papers">
      <li><a href="papers/treempo.pdf" title="download">TreeMPO: Fine-Grained Credit Assignment for LLM Training via Token-Level Trajectory Branching</a></li>
      <li><a href="https://aclanthology.org/2026.acl-long.2039/" title="link">Lost in Execution: On the Multilingual Robustness of Tool Calling in Large Language Models</a></li>
      <li><a href="papers/street_level.pdf" title="download">Street-Level Competitive Ride-Hailing with Fixed-Rival Defensive PSRO</a></li>
      <li><a href="papers/fairness_or_fluency.pdf" title="download">Fairness or Fluency? An Investigation into Language Bias of Pairwise LLM-as-a-Judge</a></li>
      <li><a href="https://arxiv.org/abs/2605.11928" title="link">When Simulation Lies: A Sim-to-Real Benchmark and Domain-Randomized RL Recipe for Tool-Use Agents</a></li>
      <li><a href="papers/latent_skill.pdf" title="download">SkiLT: What Agent Reinforcement Learning Actually Learns from a Latent Skill Library</a></li>
      <li><a href="machine_learning_paper/paper_submitted.docx" title="download">Predicting the Transfer Intentions of Specialist Nurses through Machine Learning</a></li>
    </ul>
  </section>

  <section class="content-section" aria-labelledby="projects-heading">
    <h2 id="projects-heading" class="section-heading">Projects and Materials</h2>
    <ul class="link-grid">
      <li><a href="capstone/index.md">SJTU Undergraduate Capstone Project (毕业设计)</a></li>
      <li><a href="crafty_piggies/index.md">Crafty Piggies 3D for Game Development Course</a></li>
      <li><a href="https://glassboxwisdom.com/">Thoughts on Explicit and Explainable AI</a></li>
      <li><a href="proposal/index.md">Research Project Proposal for a "Backboned" Explainable AI</a></li>
      <li><a href="zelda_game/index.md">Zelda Game for Game Development Course</a></li>
      <li><a href="piano_sheets/index.md">Transcribed Piano Sheets</a></li>
      <li><a href="transcripts/index.md">Transcripts and TOEFL Score</a></li>
      <li><a href="resume_general.pdf" download>Resume</a></li>
    </ul>
  </section>
</main>
