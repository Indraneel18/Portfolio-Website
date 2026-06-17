<script>
  const projects = [
    {
      title: 'Blackjack Game',
      description:
        'A browser-based card game with score tracking, randomized dealing, and classic Blackjack rules.',
      technologies: ['JavaScript', 'HTML5', 'CSS3'],
      accent: '#ffc928',
      className: 'blackjack',
      codeUrl: 'https://github.com/Indraneel18/Black-jack'
    },
    {
      title: 'Lead Tracker',
      description:
        'A lightweight chrome extension for saving useful links and keeping sales leads organized in one place.',
      technologies: ['JavaScript', 'HTML5', 'CSS3'],
      accent: '#57d6a4',
      className: 'lead-tracker',
      codeUrl: 'https://github.com/Indraneel18/Lead_Tracker'
    }
  ];

  /** @param {HTMLElement} node */
  function revealOnScroll(node) {
    if (!('IntersectionObserver' in window)) {
      node.classList.add('is-visible');
      return { destroy() {} };
    }

    const observer = new IntersectionObserver(
      ([entry]) => {
        if (entry.isIntersecting) {
          node.classList.add('is-visible');
          observer.disconnect();
        }
      },
      { threshold: 0.14 }
    );

    observer.observe(node);

    return {
      destroy() {
        observer.disconnect();
      }
    };
  }
</script>

<section
  class="projects-section"
  id="projects"
  aria-labelledby="projects-heading"
  use:revealOnScroll
>
  <div class="projects-container">
    <div class="projects-heading">
      <svg viewBox="0 0 64 52" aria-hidden="true">
        <path d="M7 10h20l5 6h25v29H7V10Z" />
        <path d="m22 35-6-6 6-6M42 23l6 6-6 6M35 21l-6 16" />
      </svg>
      <h2 id="projects-heading">My <span>Projects</span></h2>
    </div>

    <p class="projects-intro">
      A few things I have built while learning and exploring frontend development.
    </p>

    <div class="projects-grid">
      {#each projects as project, index}
        <article
          class="project-card"
          style={`--delay: ${index * 140}ms; --accent: ${project.accent}`}
        >
          <div class={`project-preview ${project.className}`} aria-hidden="true">
            {#if project.className === 'blackjack'}
              <div class="game-table">
                <span class="table-label">BLACKJACK</span>
                <div class="playing-cards">
                  <span class="playing-card red">A<span>♥</span></span>
                  <span class="playing-card">K<span>♠</span></span>
                </div>
                <span class="game-score">You win! 21</span>
              </div>
            {:else}
              <div class="tracker-window">
                <div class="window-bar"><i></i><i></i><i></i></div>
                <div class="tracker-content">
                  <span class="tracker-title">LEAD TRACKER</span>
                  <span class="tracker-input">Paste a link here...</span>
                  <span class="tracker-button">SAVE LEAD</span>
                  <span class="tracker-link">portfolio-inspiration.com</span>
                  <span class="tracker-link short">javascript-resources.dev</span>
                </div>
              </div>
            {/if}
          </div>

          <div class="project-content">
            <div class="project-number" aria-hidden="true">0{index + 1}</div>
            <h3>{project.title}</h3>
            <p>{project.description}</p>

            <ul class="technology-list" aria-label={`${project.title} technologies`}>
              {#each project.technologies as technology}
                <li>{technology}</li>
              {/each}
            </ul>

            <div class="project-links">
              <a class="code-link" href={project.codeUrl} target="_blank" rel="noreferrer">
                <svg viewBox="0 0 24 24" aria-hidden="true">
                  <path d="m9 18-6-6 6-6M15 6l6 6-6 6" />
                </svg>
                View Code
              </a>
            </div>
          </div>
        </article>
      {/each}
    </div>
  </div>
</section>

<style>
  .projects-section {
    overflow: hidden;
    padding: 78px 24px 104px;
    background:
      radial-gradient(circle at 12% 14%, rgba(104, 29, 255, 0.2), transparent 28%),
      radial-gradient(circle at 88% 82%, rgba(255, 201, 40, 0.1), transparent 25%),
      #08031d;
    color: #ffffff;
  }

  .projects-container {
    width: min(1250px, 100%);
    margin: 0 auto;
  }

  .projects-heading {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    opacity: 0;
    transform: translateY(-20px);
    transition: opacity 0.65s ease, transform 0.65s ease;
  }

  .projects-heading svg {
    width: 54px;
    height: 46px;
    fill: none;
    stroke: currentColor;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 4;
  }

  .projects-heading h2 {
    margin: 0;
    font-size: clamp(2.2rem, 5vw, 3.15rem);
    line-height: 1;
    font-weight: 900;
  }

  .projects-heading span {
    color: #ffc928;
  }

  .projects-intro {
    max-width: 680px;
    margin: 20px auto 38px;
    color: #cbc6df;
    font-size: clamp(0.96rem, 2vw, 1.12rem);
    line-height: 1.6;
    text-align: center;
    opacity: 0;
    transform: translateY(16px);
    transition: opacity 0.65s ease 0.08s, transform 0.65s ease 0.08s;
  }

  .projects-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 28px;
  }

  .project-card {
    overflow: hidden;
    border: 1px solid rgba(255, 255, 255, 0.11);
    border-radius: 18px;
    background: #130a32;
    opacity: 0;
    box-shadow: 0 22px 45px rgba(0, 0, 0, 0.28);
    transform: translateY(45px);
    transition:
      opacity 0.7s ease var(--delay),
      transform 0.7s cubic-bezier(0.2, 0.75, 0.25, 1) var(--delay),
      border-color 0.25s ease,
      box-shadow 0.25s ease;
  }

  .project-card:hover {
    border-color: color-mix(in srgb, var(--accent) 55%, transparent);
    box-shadow: 0 26px 55px rgba(0, 0, 0, 0.4);
    transform: translateY(-6px);
  }

  .project-preview {
    display: grid;
    min-height: 290px;
    place-items: center;
    padding: 28px;
  }

  .blackjack {
    background: linear-gradient(145deg, #116344, #073b2c);
  }

  .game-table {
    display: grid;
    width: min(330px, 86%);
    min-height: 200px;
    place-items: center;
    border: 3px solid rgba(255, 218, 118, 0.72);
    border-radius: 50%;
    box-shadow: inset 0 0 40px rgba(0, 0, 0, 0.3), 0 18px 28px rgba(0, 0, 0, 0.28);
  }

  .table-label {
    color: #ffdc70;
    font-size: 0.8rem;
    font-weight: 900;
    letter-spacing: 0.24em;
  }

  .playing-cards {
    display: flex;
    margin: -4px 0;
  }

  .playing-card {
    display: flex;
    width: 62px;
    height: 86px;
    flex-direction: column;
    justify-content: space-between;
    margin: 0 -8px;
    padding: 8px;
    border-radius: 7px;
    background: #ffffff;
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.24);
    color: #16131c;
    font-size: 1.15rem;
    font-weight: 900;
    transform: rotate(-7deg);
  }

  .playing-card + .playing-card {
    transform: rotate(7deg) translateY(4px);
  }

  .playing-card span {
    align-self: center;
    font-size: 1.7rem;
  }

  .playing-card.red {
    color: #dc2638;
  }

  .game-score {
    color: #ffffff;
    font-size: 0.9rem;
    font-weight: 800;
  }

  .lead-tracker {
    background: linear-gradient(145deg, #d9fff0, #68d8aa);
  }

  .tracker-window {
    width: min(380px, 92%);
    overflow: hidden;
    border-radius: 11px;
    background: #ffffff;
    box-shadow: 0 20px 36px rgba(10, 62, 46, 0.28);
  }

  .window-bar {
    display: flex;
    gap: 6px;
    padding: 11px 13px;
    background: #18233a;
  }

  .window-bar i {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: #ff6b67;
  }

  .window-bar i:nth-child(2) {
    background: #ffc928;
  }

  .window-bar i:nth-child(3) {
    background: #57d6a4;
  }

  .tracker-content {
    display: flex;
    min-height: 180px;
    flex-direction: column;
    align-items: flex-start;
    padding: 20px;
  }

  .tracker-title {
    margin-bottom: 14px;
    color: #173b30;
    font-size: 0.9rem;
    font-weight: 900;
    letter-spacing: 0.08em;
  }

  .tracker-input {
    width: 100%;
    box-sizing: border-box;
    padding: 9px 10px;
    border: 2px solid #57b991;
    color: #8a9691;
    font-size: 0.7rem;
  }

  .tracker-button {
    margin: 8px 0 14px;
    padding: 8px 13px;
    background: #16845d;
    color: white;
    font-size: 0.65rem;
    font-weight: 900;
  }

  .tracker-link {
    margin-top: 6px;
    color: #16845d;
    font-size: 0.7rem;
    font-weight: 700;
  }

  .project-content {
    position: relative;
    padding: 30px;
  }

  .project-number {
    position: absolute;
    top: 22px;
    right: 26px;
    color: rgba(255, 255, 255, 0.09);
    font-size: 3.8rem;
    line-height: 1;
    font-weight: 900;
  }

  .project-content h3 {
    position: relative;
    margin: 0;
    color: var(--accent);
    font-size: clamp(1.55rem, 3vw, 2rem);
    font-weight: 900;
  }

  .project-content p {
    position: relative;
    min-height: 76px;
    margin: 14px 0 20px;
    color: #cbc6df;
    font-size: 0.98rem;
    line-height: 1.6;
  }

  .technology-list {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin: 0 0 26px;
    padding: 0;
    list-style: none;
  }

  .technology-list li {
    padding: 7px 11px;
    border: 1px solid rgba(255, 255, 255, 0.13);
    border-radius: 999px;
    background: rgba(255, 255, 255, 0.06);
    color: #f1eefb;
    font-size: 0.78rem;
    font-weight: 700;
  }

  .project-links {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  .project-links a {
    display: inline-flex;
    min-height: 44px;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 0 17px;
    border: 2px solid var(--accent);
    border-radius: 7px;
    background: var(--accent);
    color: #100a25;
    font-size: 0.88rem;
    font-weight: 900;
    text-decoration: none;
    transition: transform 0.2s ease, filter 0.2s ease;
  }

  .project-links a:hover {
    filter: brightness(1.08);
    transform: translateY(-2px);
  }

  .project-links .code-link {
    background: transparent;
    color: #ffffff;
  }

  .project-links svg {
    width: 18px;
    height: 18px;
    fill: none;
    stroke: currentColor;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 2;
  }

  .projects-section:global(.is-visible) .projects-heading,
  .projects-section:global(.is-visible) .projects-intro,
  .projects-section:global(.is-visible) .project-card {
    opacity: 1;
    transform: translateY(0);
  }

  @media (max-width: 820px) {
    .projects-grid {
      grid-template-columns: 1fr;
    }

    .project-content p {
      min-height: auto;
    }
  }

  @media (max-width: 520px) {
    .projects-section {
      padding: 58px 16px 78px;
    }

    .projects-heading {
      gap: 8px;
    }

    .projects-heading svg {
      width: 42px;
      height: 36px;
    }

    .project-preview {
      min-height: 235px;
      padding: 18px;
    }

    .project-content {
      padding: 24px 22px 26px;
    }

    .project-number {
      right: 18px;
      font-size: 3rem;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .projects-heading,
    .projects-intro,
    .project-card {
      opacity: 1;
      transform: none;
      transition: none;
    }
  }
</style>
