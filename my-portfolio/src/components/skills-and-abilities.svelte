<script>
  import cLogo from '../assets/C logo.jpeg';

  const skills = [
    {
      name: 'GitHub',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/github/github-original.svg',
      invert: true
    },
    {
      name: 'Git',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/git/git-original.svg'
    },
    {
      name: 'Vercel',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vercel/vercel-original.svg',
      invert: true
    },
    {
      name: 'CSS3',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/css3/css3-original.svg'
    },
    {
      name: 'Svelte',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/svelte/svelte-original.svg'
    },
    {
      name: 'Tailwind CSS',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original.svg'
    },
    {
      name: 'JavaScript',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg'
    },
    {
      name: 'C',
      icon: cLogo
    },
    {
      name: 'C++',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/cplusplus/cplusplus-original.svg'
    },
    {
      name: 'WordPress',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/wordpress/wordpress-plain.svg'
    },
    {
      name: 'PHP',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/php/php-original.svg'
    },
    {
      name: 'HTML5',
      icon: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/html5/html5-original.svg'
    }
  ];
</script>

<section class="skills-section" id="skills" aria-labelledby="skills-heading">
  <div class="skills-heading">
    <svg viewBox="0 0 64 48" aria-hidden="true">
      <path d="M11 6h42a5 5 0 0 1 5 5v23a5 5 0 0 1-5 5H11a5 5 0 0 1-5-5V11a5 5 0 0 1 5-5Z" />
      <path d="M25 16 18 23l7 7M39 16l7 7-7 7" />
      <path d="M26 45h12M32 39v6M3 45h58" />
    </svg>
    <h2 id="skills-heading">Skills &amp; <span>Abilities</span></h2>
  </div>

  <div class="skills-panel">
    <div class="skills-grid" aria-label="Technology skills">
      {#each skills as skill}
        <article class="skill-card">
          <img class:invert-icon={skill.invert} src={skill.icon} alt="" loading="lazy" aria-hidden="true" />
          <h3>{skill.name}</h3>
        </article>
      {/each}
    </div>
  </div>
</section>

<style>
  .skills-section {
    padding: 72px 24px 86px;
    background: linear-gradient(180deg, #5d00a8 0%, #6500e8 100%);
    color: #ffffff;
  }

  .skills-heading {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    margin: 0 auto 36px;
  }

  .skills-heading svg {
    width: 56px;
    height: 44px;
    fill: none;
    stroke: currentColor;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 5;
  }

  .skills-heading h2 {
    margin: 0;
    font-size: clamp(2.25rem, 5vw, 3.15rem);
    line-height: 1;
    font-weight: 900;
    letter-spacing: 0;
  }

  .skills-heading span {
    color: #fff200;
  }

  .skills-panel {
    width: min(1400px, 100%);
    margin: 0 auto;
    padding: 25px;
    border-radius: 11px;
    background: rgba(41, 0, 88, 0.82);
  }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: clamp(20px, 2.3vw, 42px) clamp(18px, 2vw, 28px);
  }

  .skill-card {
    display: grid;
    grid-template-rows: 72px auto;
    place-items: center;
    min-height: 148px;
    padding: 24px 16px 18px;
    border-radius: 11px;
    background: #050018;
    box-shadow: inset 0 0 0 1px rgba(255, 255, 255, 0.02);
    transition: transform 0.22s ease, background 0.22s ease, box-shadow 0.22s ease;
  }

  .skill-card:hover {
    transform: translateY(-5px);
    background: #090024;
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.24);
  }

  .skill-card img {
    width: 62px;
    height: 62px;
    object-fit: contain;
  }

  .skill-card .invert-icon {
    filter: invert(1);
  }

  .skill-card h3 {
    margin: 10px 0 0;
    color: #ffffff;
    font-size: clamp(1.2rem, 2vw, 1.65rem);
    line-height: 1.15;
    font-weight: 500;
    text-align: center;
  }

  @media (max-width: 1040px) {
    .skills-grid {
      grid-template-columns: repeat(3, minmax(0, 1fr));
    }
  }

  @media (max-width: 720px) {
    .skills-section {
      padding: 58px 16px 72px;
    }

    .skills-panel {
      padding: 18px;
    }

    .skills-grid {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }
  }

  @media (max-width: 460px) {
    .skills-heading {
      gap: 8px;
    }

    .skills-heading svg {
      width: 42px;
      height: 34px;
      stroke-width: 5.4;
    }

    .skills-panel {
      padding: 14px;
    }

    .skills-grid {
      gap: 14px;
    }

    .skill-card {
      grid-template-rows: 58px auto;
      min-height: 124px;
      padding: 18px 10px 14px;
    }

    .skill-card img {
      width: 50px;
      height: 50px;
    }

    .skill-card h3 {
      font-size: 1.03rem;
    }
  }
</style>
