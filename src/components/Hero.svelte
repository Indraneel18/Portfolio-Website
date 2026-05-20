<script>
  import { onMount } from 'svelte';
  import profilePhoto from '../assets/Indraneel.png';

  /** @type {HTMLCanvasElement | null} */
  let canvas = null;

   /** @type {number | null} */
  let animationFrame = null;

  /** @type {{x:number,y:number,vx:number,vy:number,baseVx:number,baseVy:number,radius:number}[]} */
  let points = [];

  onMount(() => {
    if (!canvas) return;
    const context = canvas.getContext('2d');
    if (!context) return;
    const mediaQuery = window.matchMedia('(prefers-reduced-motion: reduce)');
    let width = 0;
    let height = 0;
    const movementSpeed = 1.65;
    const mouse = {
      x: 0,
      y: 0,
      active: false
    };

    const createPoints = () => {
      const count = Math.max(119, Math.floor((width * height) / 12940));

      points = Array.from({ length: count }, (_, index) => {
        const edgeBias = index % 4;
        const x =
          edgeBias === 0 ? Math.random() * width * 0.28 :
          edgeBias === 1 ? width - Math.random() * width * 0.28 :
          Math.random() * width;
        const y =
          edgeBias === 2 ? Math.random() * height * 0.24 :
          edgeBias === 3 ? height - Math.random() * height * 0.24 :
          Math.random() * height;

        const vx = (Math.random() - 0.5) * movementSpeed;
        const vy = (Math.random() - 0.5) * movementSpeed;

        return {
          x,
          y,
          vx,
          vy,
          baseVx: vx,
          baseVy: vy,
          radius: Math.random() * 2.8 + 2.1
        };
      });
    };

    const resize = () => {
      if (!canvas) return;
      const pixelRatio = window.devicePixelRatio || 1;
      width = canvas.offsetWidth;
      height = canvas.offsetHeight;
      canvas.width = width * pixelRatio;
      canvas.height = height * pixelRatio;
      context.setTransform(pixelRatio, 0, 0, pixelRatio, 0, 0);
      createPoints();
    };

    const draw = () => {
      context.clearRect(0, 0, width, height);

      for (const point of points) {
        if (mouse.active) {
          const dx = point.x - mouse.x;
          const dy = point.y - mouse.y;
          const distance = Math.hypot(dx, dy);
          const repelRadius = 165;

          if (distance < repelRadius && distance > 0.01) {
            const force = (1 - distance / repelRadius) * 1.75;
            point.vx += (dx / distance) * force;
            point.vy += (dy / distance) * force;
          }
        }

        point.vx += (point.baseVx - point.vx) * 0.035;
        point.vy += (point.baseVy - point.vy) * 0.035;
        point.vx *= 0.985;
        point.vy *= 0.985;

        point.x += point.vx;
        point.y += point.vy;

        if (point.x < -20 || point.x > width + 20) point.vx *= -1;
        if (point.y < -20 || point.y > height + 20) point.vy *= -1;
      }

      for (let index = 0; index < points.length; index += 1) {
        const point = points[index];

        for (let nextIndex = index + 1; nextIndex < points.length; nextIndex += 1) {
          const nextPoint = points[nextIndex];
          const distance = Math.hypot(point.x - nextPoint.x, point.y - nextPoint.y);
          const maxDistance = 160;

          if (distance < maxDistance) {
            context.beginPath();
            context.moveTo(point.x, point.y);
            context.lineTo(nextPoint.x, nextPoint.y);
            context.strokeStyle = `rgba(92, 99, 106, ${0.22 * (1 - distance / maxDistance)})`;
            context.lineWidth = 1;
            context.stroke();
          }
        }
      }

      for (const point of points) {
        context.beginPath();
        context.arc(point.x, point.y, point.radius, 0, Math.PI * 2);
        context.fillStyle = 'rgba(76, 80, 84, 0.72)';
        context.fill();
      }

      if (!mediaQuery.matches) {
        animationFrame = requestAnimationFrame(draw);
      }
    };

    resize();
    draw();

    /** @param {PointerEvent} event */
    const updateMouse = (event) => {
      if (!canvas) return;
      const rect = canvas.getBoundingClientRect();
      const x = event.clientX - rect.left;
      const y = event.clientY - rect.top;

      mouse.x = x;
      mouse.y = y;
      mouse.active = x >= 0 && x <= rect.width && y >= 0 && y <= rect.height;
    };

    const clearMouse = () => {
      mouse.active = false;
    };

    window.addEventListener('resize', resize);
    window.addEventListener('pointermove', updateMouse);
    window.addEventListener('pointerleave', clearMouse);

    return () => {
      window.removeEventListener('resize', resize);
      window.removeEventListener('pointermove', updateMouse);
      window.removeEventListener('pointerleave', clearMouse);
      if (animationFrame) cancelAnimationFrame(animationFrame);
    };
  });
</script>

<section class="hero" id="home" aria-label="Introduction">
  <canvas class="neural-background" bind:this={canvas} aria-hidden="true"></canvas>

  <div class="hero-content">
    <div class="hero-copy">
      <p class="eyebrow">Hi There,</p>
      <h1>I'm Indraneel <span>Chowdhury</span></h1>
      <p class="role">I Am Into <span>Web Development</span> |</p>

      <a class="about-link" href="#about">
        About Me
        <svg viewBox="0 0 24 24" aria-hidden="true">
          <path d="M12 5v14m0 0 6-6m-6 6-6-6" />
        </svg>
      </a>

      <div class="social-links" aria-label="Social links">
        <a href="https://github.com/" aria-label="GitHub">
          <svg><use href="/icons.svg#github-icon" /></svg>
        </a>
        <a href="https://x.com/" aria-label="X">
          <svg><use href="/icons.svg#x-icon" /></svg>
        </a>
        <a href="https://www.linkedin.com/" aria-label="LinkedIn">
          <span>in</span>
        </a>
        <a href="#contact" aria-label="Contact">
          <svg><use href="/icons.svg#social-icon" /></svg>
        </a>
      </div>
    </div>

    <div class="hero-photo" aria-label="Indraneel Sable profile photo">
      <div class="photo-ring">
        <img src={profilePhoto} alt="Indraneel Sable" />
      </div>
    </div>
  </div>
</section>

<style>
  .hero {
    position: relative;
    min-height: calc(100vh - 78px);
    overflow: hidden;
    background: #f7f7f7;
    color: #061f55;
  }

  .neural-background {
    position: absolute;
    inset: 0;
    width: 100%;
    height: 100%;
    opacity: 0.9;
  }

  .hero-content {
    position: relative;
    z-index: 1;
    display: grid;
    grid-template-columns: minmax(280px, 1fr) minmax(280px, 0.9fr);
    align-items: center;
    gap: clamp(2rem, 7vw, 7rem);
    width: min(1220px, calc(100% - 48px));
    min-height: calc(100vh - 78px);
    margin: 0 auto;
    padding: clamp(3rem, 8vh, 6rem) 0;
  }

  .hero-copy {
    max-width: 620px;
  }

  .eyebrow,
  h1 {
    margin: 0;
    font-size: clamp(3rem, 6vw, 5.2rem);
    line-height: 1.08;
    font-weight: 800;
    letter-spacing: 0;
  }

  h1 span {
    color: #ff7300;
  }

  .role {
    margin: 2rem 0 1.8rem;
    color: #090909;
    font-size: clamp(1.45rem, 2.2vw, 2rem);
    font-weight: 800;
  }

  .role span {
    color: #970d13;
  }

  .about-link {
    display: inline-flex;
    align-items: center;
    gap: 0.55rem;
    min-height: 58px;
    padding: 0 2.1rem;
    border-radius: 999px;
    background: #2b05be;
    color: #ffffff;
    font-size: 1.25rem;
    font-weight: 800;
    text-decoration: none;
    box-shadow: 0 14px 24px rgba(43, 5, 190, 0.28);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .about-link:hover {
    transform: translateY(-2px);
    box-shadow: 0 18px 30px rgba(43, 5, 190, 0.32);
  }

  .about-link svg {
    width: 22px;
    height: 22px;
    fill: none;
    stroke: currentColor;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 2.4;
  }

  .social-links {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 2.6rem;
  }

  .social-links a {
    display: inline-grid;
    width: 54px;
    height: 54px;
    place-items: center;
    border-radius: 50%;
    background: #080016;
    color: #03c8ff;
    text-decoration: none;
    transition: transform 0.2s ease, background 0.2s ease;
  }

  .social-links a:hover {
    transform: translateY(-3px);
    background: #180057;
  }

  .social-links svg {
    width: 24px;
    height: 24px;
    filter: invert(58%) sepia(91%) saturate(2045%) hue-rotate(151deg) brightness(104%) contrast(104%);
  }

  .social-links span {
    font-size: 1.2rem;
    font-weight: 900;
  }

  .hero-photo {
    display: flex;
    justify-content: center;
    perspective: 900px;
  }

  .photo-ring {
    position: relative;
    display: block;
    width: min(34rem, 86vw);
    aspect-ratio: 1;
    overflow: hidden;
    border-radius: 50%;
    background: #ffc700;
    box-shadow:
      0 30px 45px rgba(0, 0, 0, 0.18),
      inset 0 -18px 28px rgba(177, 114, 0, 0.08);
    transform: rotateX(2deg) rotateY(-5deg);
  }

  .photo-ring::after {
    position: absolute;
    right: 16%;
    bottom: 3%;
    left: 16%;
    height: 14%;
    border-radius: 50%;
    background: rgba(0, 0, 0, 0.22);
    content: '';
    filter: blur(20px);
  }

  .photo-ring img {
    position: absolute;
    right: 50%;
    bottom: 0;
    z-index: 1;
    width: 84%;
    max-height: 96%;
    object-fit: contain;
    filter: grayscale(1) contrast(1.06) drop-shadow(0 18px 14px rgba(0, 0, 0, 0.24));
    transform: translateX(50%) translateZ(54px);
  }

  @media (max-width: 820px) {
    .hero-content {
      grid-template-columns: 1fr;
      gap: 2.2rem;
      text-align: center;
      padding-top: 2.5rem;
    }

    .hero-copy {
      margin: 0 auto;
    }

    .social-links,
    .hero-photo {
      justify-content: center;
    }

    .hero-photo {
      order: -1;
    }

    .photo-ring {
      width: min(24rem, 78vw);
    }
  }

  @media (max-width: 520px) {
    .hero-content {
      width: min(100% - 32px, 1220px);
      min-height: auto;
    }

    .eyebrow,
    h1 {
      font-size: clamp(2.45rem, 14vw, 3.4rem);
    }

    .about-link {
      min-height: 52px;
      padding: 0 1.45rem;
      font-size: 1.05rem;
    }

    .social-links a {
      width: 48px;
      height: 48px;
    }
  }
</style>
