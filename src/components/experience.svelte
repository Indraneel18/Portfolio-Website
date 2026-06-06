<script>
  import hnnoixLogo from '../assets/hnnoix.jpg';

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
      { threshold: 0.16 }
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
  class="experience-section"
  id="experience"
  aria-labelledby="experience-heading"
  use:revealOnScroll
>
  <div class="experience-container">
    <div class="experience-heading">
      <svg viewBox="0 0 64 54" aria-hidden="true">
        <path d="M22 14V9a5 5 0 0 1 5-5h10a5 5 0 0 1 5 5v5" />
        <rect x="5" y="14" width="54" height="35" rx="5" />
        <path d="M5 27c14 8 40 8 54 0M27 28h10v7H27z" />
      </svg>
      <h2 id="experience-heading">My <span>Experience</span></h2>
    </div>

    <p class="experience-intro">
      Where learning meets real-world problem solving and meaningful development work.
    </p>

    <article class="experience-card">
      <div class="logo-wrap">
        <img src={hnnoixLogo} alt="HNNOIX logo" />
      </div>
      <div>
        <h3>HNNOIX</h3>
        <h4>Software Developer</h4>
        <p>Internship</p>
      </div>
    </article>
  </div>
</section>

<style>
  .experience-section {
    overflow: hidden;
    padding: 78px 24px 100px;
    border-top: 2px solid #3d18d8;
    background:
      radial-gradient(circle at 90% 12%, rgba(124, 9, 189, 0.1), transparent 28%),
      linear-gradient(180deg, #f7f9ff 0%, #eaf0ff 100%);
    color: #17191f;
  }

  .experience-container {
    width: min(900px, 100%);
    margin: 0 auto;
  }

  .experience-heading {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 12px;
    opacity: 0;
    transform: translateY(-20px);
    transition: opacity 0.65s ease, transform 0.65s ease;
  }

  .experience-heading svg {
    width: 54px;
    height: 46px;
    fill: none;
    stroke: #17191f;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 3.5;
  }

  .experience-heading h2 {
    margin: 0;
    font-size: clamp(2.2rem, 5vw, 3.15rem);
    line-height: 1;
    font-weight: 900;
  }

  .experience-heading span {
    color: #7c09bd;
  }

  .experience-intro {
    margin: 20px auto 0;
    color: #4c5162;
    font-size: clamp(0.96rem, 2vw, 1.12rem);
    line-height: 1.6;
    text-align: center;
    opacity: 0;
    transform: translateY(16px);
    transition: opacity 0.65s ease 0.08s, transform 0.65s ease 0.08s;
  }

  .experience-card {
    display: flex;
    align-items: center;
    gap: 28px;
    width: min(620px, 100%);
    box-sizing: border-box;
    margin: 48px auto 0;
    padding: 28px 34px;
    border: 1px solid rgba(61, 24, 216, 0.12);
    border-left: 6px solid #7c09bd;
    border-radius: 16px;
    background: #ffffff;
    opacity: 0;
    box-shadow: 0 18px 38px rgba(29, 38, 82, 0.16);
    transform: translateY(40px);
    transition:
      opacity 0.7s ease 0.12s,
      transform 0.7s cubic-bezier(0.2, 0.75, 0.25, 1) 0.12s,
      box-shadow 0.25s ease;
  }

  .experience-card:hover {
    box-shadow: 0 24px 48px rgba(29, 38, 82, 0.22);
    transform: translateY(-4px);
  }

  .logo-wrap {
    display: grid;
    width: 112px;
    height: 112px;
    flex: 0 0 auto;
    overflow: hidden;
    place-items: center;
    border-radius: 14px;
    background: #ffffff;
    box-shadow: 0 8px 20px rgba(29, 38, 82, 0.14);
  }

  .logo-wrap img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  .experience-card h3 {
    margin: 0;
    color: #063886;
    font-size: clamp(1.8rem, 4vw, 2.45rem);
    font-weight: 900;
    letter-spacing: 0.03em;
  }

  .experience-card p {
    display: inline-block;
    margin: 12px 0 0;
    padding: 7px 13px;
    border-radius: 999px;
    background: #f0edff;
    color: #7c09bd;
    font-size: 0.9rem;
    font-weight: 800;
  }

  .experience-card h4 {
    margin: 6px 0 0;
    color: #252938;
    font-size: clamp(1rem, 2vw, 1.2rem);
    font-weight: 700;
  }

  .experience-section:global(.is-visible) .experience-heading,
  .experience-section:global(.is-visible) .experience-intro,
  .experience-section:global(.is-visible) .experience-card {
    opacity: 1;
    transform: translateY(0);
  }

  @media (max-width: 520px) {
    .experience-section {
      padding: 58px 16px 76px;
    }

    .experience-heading {
      gap: 8px;
    }

    .experience-heading svg {
      width: 42px;
      height: 36px;
    }

    .experience-card {
      flex-direction: column;
      margin-top: 36px;
      padding: 26px 20px;
      text-align: center;
    }

    .logo-wrap {
      width: 100px;
      height: 100px;
    }
  }

  @media (prefers-reduced-motion: reduce) {
    .experience-heading,
    .experience-intro,
    .experience-card {
      opacity: 1;
      transform: none;
      transition: none;
    }
  }
</style>
