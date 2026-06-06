<script>
  import sbaImage from '../assets/SBA.jpg';
  import sotImage from '../assets/SOT.jpg';

  const education = [
    {
      degree: 'Bachelor of Technology in Electronics and Communication Engineering',
      institution: 'School of Technology, NEHU | Central University',
      period: '2024-2028',
      status: 'Pursuing',
      image: sotImage
    },
    {
      degree: 'Higher Secondary Certificate in Science',
      institution: 'Salt Brook Academy | AHSEC',
      period: '2022-2024',
      status: 'Completed',
      image: sbaImage
    }
  ];

  /** @param {HTMLElement} node */
  function revealOnScroll(node) {
    if (!('IntersectionObserver' in window)) {
      node.classList.add('is-visible');
      return {
        destroy() {}
      };
    }

    const observer = new IntersectionObserver(
      ([entry]) => {
        node.classList.toggle('is-visible', entry.intersectionRatio >= 0.16);
      },
      {
        threshold: [0, 0.16],
        rootMargin: '-8% 0px -8%'
      }
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
  class="education-section"
  id="education"
  aria-labelledby="education-heading"
  use:revealOnScroll
>
  <div class="education-container">
    <div class="education-heading">
      <svg viewBox="0 0 64 48" aria-hidden="true">
        <path d="M4 14 32 4l28 10-28 10L4 14Z" />
        <path d="M15 19v15c8 6 26 6 34 0V19" />
        <path d="M58 16v16" />
        <circle cx="58" cy="35" r="2" />
      </svg>
      <h2 id="education-heading">My <span>Education</span></h2>
    </div>

    <p class="education-intro">
      Education is not the learning of facts, but the training of the mind to think.
    </p>

    <div class="education-list">
      {#each education as item, index}
        <article class="education-card" style={`--delay: ${index * 140}ms`}>
          <div class="education-image">
            <img src={item.image} alt="" loading="lazy" aria-hidden="true" />
          </div>

          <div class="education-details">
            <h3>{item.degree}</h3>
            <p>{item.institution}</p>
            <strong>{item.period} <span aria-hidden="true">|</span> {item.status}</strong>
          </div>
        </article>
      {/each}
    </div>
  </div>
</section>

<style>
  .education-section {
    overflow: hidden;
    padding: 72px 24px 100px;
    border-top: 2px solid #3d18d8;
    background: #eaf0ff;
    color: #111111;
  }

  .education-container {
    width: min(1250px, 100%);
    margin: 0 auto;
  }

  .education-heading {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    opacity: 0;
    transform: translateY(-22px);
    transition: opacity 0.65s ease, transform 0.65s ease;
  }

  .education-heading svg {
    width: 54px;
    height: 44px;
    fill: #17191f;
    stroke: #17191f;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 3;
  }

  .education-heading h2 {
    margin: 0;
    font-size: clamp(2.2rem, 5vw, 3.15rem);
    line-height: 1;
    font-weight: 900;
  }

  .education-heading span {
    color: #7c09bd;
  }

  .education-intro {
    margin: 20px auto 28px;
    opacity: 0;
    font-size: clamp(0.95rem, 2vw, 1.15rem);
    font-weight: 500;
    line-height: 1.5;
    text-align: center;
    transform: translateY(18px);
    transition: opacity 0.65s ease 0.1s, transform 0.65s ease 0.1s;
  }

  .education-list {
    display: grid;
    gap: 24px;
  }

  .education-card {
    display: grid;
    grid-template-columns: 310px minmax(0, 1fr);
    min-height: 190px;
    overflow: hidden;
    border-radius: 7px;
    background: #ffffff;
    opacity: 0;
    box-shadow: 0 10px 20px rgba(25, 35, 70, 0.2);
    transform: translateX(-70px);
    transition:
      opacity 0.75s ease,
      transform 0.75s cubic-bezier(0.2, 0.75, 0.25, 1),
      box-shadow 0.25s ease;
  }

  .education-card:nth-child(even) {
    transform: translateX(70px);
  }

  .education-card:hover {
    box-shadow: 0 16px 30px rgba(25, 35, 70, 0.26);
  }

  .education-image {
    min-height: 190px;
    overflow: hidden;
    background: #d9dfec;
  }

  .education-image img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.45s ease;
  }

  .education-card:hover img {
    transform: scale(1.045);
  }

  .education-details {
    align-self: center;
    padding: 28px 26px;
  }

  .education-details h3 {
    margin: 0;
    color: #063886;
    font-size: clamp(1.35rem, 2.5vw, 2rem);
    line-height: 1.2;
    font-weight: 800;
  }

  .education-details p {
    margin: 14px 0 18px;
    font-size: clamp(0.96rem, 1.8vw, 1.14rem);
    line-height: 1.45;
  }

  .education-details strong {
    color: #168000;
    font-size: clamp(1.05rem, 2vw, 1.45rem);
    line-height: 1.3;
    font-weight: 700;
  }

  .education-section:global(.is-visible) .education-heading,
  .education-section:global(.is-visible) .education-intro,
  .education-section:global(.is-visible) .education-card {
    opacity: 1;
    transform: translate(0);
  }

  .education-section:global(.is-visible) .education-card {
    transition-delay: var(--delay), var(--delay), 0s;
  }

  @media (max-width: 760px) {
    .education-section {
      padding: 58px 16px 76px;
    }

    .education-card {
      grid-template-columns: 1fr;
    }

    .education-image {
      min-height: 220px;
      max-height: 280px;
    }

    .education-details {
      padding: 24px 22px 28px;
    }
  }

  @media (max-width: 460px) {
    .education-heading {
      gap: 8px;
    }

    .education-heading svg {
      width: 42px;
      height: 34px;
    }

    .education-intro {
      margin-top: 16px;
    }

    .education-image {
      min-height: 180px;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .education-heading,
    .education-intro,
    .education-card {
      opacity: 1;
      transform: none;
      transition: none;
    }

    .education-image img {
      transition: none;
    }
  }
</style>
