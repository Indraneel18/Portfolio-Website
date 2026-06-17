<script>
  const quickLinks = [
    { label: 'Home', href: '#home' },
    { label: 'About', href: '#about' },
    { label: 'Skills', href: '#skills' },
    { label: 'Education', href: '#education' },
    { label: 'Projects', href: '#projects' },
    { label: 'Experience', href: '#experience' }
  ];

  const currentYear = new Date().getFullYear();
</script>

<footer id="contact">
  <div class="footer-content">
    <div class="footer-about">
      <h2>Indraneel's Portfolio</h2>
      <p>
        Thank you for visiting my personal portfolio. Connect with me and follow
        along as I continue building and learning.
      </p>
      <strong>Keep growing. Keep creating.</strong>
    </div>

    <nav class="footer-links" aria-label="Footer navigation">
      <h2>Quick Links</h2>
      <ul>
        {#each quickLinks as link}
          <li>
            <a href={link.href}>
              <span aria-hidden="true">›</span>
              {link.label}
            </a>
          </li>
        {/each}
      </ul>
    </nav>

    <div class="footer-contact">
      <h2>Contact Info</h2>

      <a href="https://mail.google.com/mail/?view=cm&fs=1&to=indraneelchowdhury1818@gmail.com" target="_blank" rel="noopener noreferrer">
        <svg viewBox="0 0 24 24" aria-hidden="true">
          <path d="M3 5h18v14H3V5Z" />
          <path d="m3 7 9 6 9-6" />
        </svg>
        indraneelchowdhury1818@gmail.com
      </a>

      <p>
        <svg viewBox="0 0 24 24" aria-hidden="true">
          <path d="M12 22s7-6.2 7-13A7 7 0 0 0 5 9c0 6.8 7 13 7 13Z" />
          <circle cx="12" cy="9" r="2.5" />
        </svg>
        Assam, India
      </p>

      <div class="social-links" aria-label="Social links">
        <a
          href="https://github.com/Indraneel18"
          target="_blank"
          rel="noreferrer"
          aria-label="GitHub"
        >
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3.3-.4 6.8-1.6 6.8-7.4A5.8 5.8 0 0 0 19.3 3 5.4 5.4 0 0 0 19.1 0S17.9-.4 15 1.5a13.4 13.4 0 0 0-6 0C6.1-.4 4.9 0 4.9 0a5.4 5.4 0 0 0-.2 3A5.8 5.8 0 0 0 3.2 7.1c0 5.8 3.5 7 6.8 7.4A4.8 4.8 0 0 0 9 18v4" />
            <path d="M9 19c-3 .9-3-1.5-4.2-2" />
          </svg>
        </a>

        <a
          href="https://mail.google.com/mail/?view=cm&fs=1&to=indraneelchowdhury1818@gmail.com"
          target="_blank"
          rel="noopener noreferrer"
          aria-label="Send email"
        >
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path d="M3 5h18v14H3V5Z" />
            <path d="m3 7 9 6 9-6" />
          </svg>
        </a>
      </div>
    </div>
  </div>

  <div class="footer-bottom">
    <p>© {currentYear} Indraneel Chowdhury. All rights reserved.</p>
    <a href="#home" aria-label="Back to top">
      <svg viewBox="0 0 24 24" aria-hidden="true">
        <path d="m6 15 6-6 6 6" />
      </svg>
    </a>
  </div>
</footer>

<style>
  footer {
    background:
      radial-gradient(circle at 15% 10%, rgba(92, 0, 168, 0.35), transparent 30%),
      #070019;
    color: #ffffff;
  }

  .footer-content {
    display: grid;
    grid-template-columns: 1.25fr 0.7fr 1.1fr;
    gap: clamp(42px, 7vw, 100px);
    width: min(1250px, calc(100% - 48px));
    margin: 0 auto;
    padding: 68px 0 54px;
  }

  h2 {
    margin: 0 0 24px;
    color: #ffffff;
    font-size: clamp(1.45rem, 3vw, 2rem);
    line-height: 1.2;
    font-weight: 800;
  }

  .footer-about p {
    max-width: 470px;
    margin: 0 0 28px;
    color: #d3cee4;
    font-size: 0.98rem;
    line-height: 1.75;
  }

  .footer-about strong {
    color: #ffc928;
    font-size: 0.96rem;
  }

  .footer-links ul {
    display: grid;
    gap: 11px;
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .footer-links a {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    color: #f3f0fa;
    font-size: 0.98rem;
    font-weight: 600;
    text-decoration: none;
    transition: color 0.2s ease, transform 0.2s ease;
  }

  .footer-links a span {
    display: grid;
    width: 18px;
    height: 18px;
    place-items: center;
    border-radius: 50%;
    background: #ffc928;
    color: #130238;
    font-size: 1.15rem;
    line-height: 1;
    font-weight: 900;
  }

  .footer-links a:hover {
    color: #ffc928;
    transform: translateX(4px);
  }

  .footer-contact > a,
  .footer-contact > p {
    display: flex;
    align-items: center;
    gap: 12px;
    margin: 0 0 18px;
    color: #dcd7e9;
    font-size: 0.94rem;
    line-height: 1.5;
    overflow-wrap: anywhere;
    text-decoration: none;
  }

  .footer-contact > a:hover {
    color: #ffc928;
  }

  .footer-contact > a svg,
  .footer-contact > p svg {
    width: 21px;
    height: 21px;
    flex: 0 0 auto;
    fill: none;
    stroke: #ffc928;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 2;
  }

  .social-links {
    display: flex;
    gap: 12px;
    margin-top: 26px;
  }

  .social-links a {
    display: grid;
    width: 46px;
    height: 46px;
    place-items: center;
    border-radius: 50%;
    background: #ffffff;
    color: #130238;
    text-decoration: none;
    transition: background 0.2s ease, color 0.2s ease, transform 0.2s ease;
  }

  .social-links a:hover {
    background: #ffc928;
    transform: translateY(-4px);
  }

  .social-links svg {
    width: 22px;
    height: 22px;
    fill: none;
    stroke: currentColor;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 1.9;
  }

  .footer-bottom {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    width: min(1250px, calc(100% - 48px));
    margin: 0 auto;
    padding: 20px 0;
    border-top: 1px solid rgba(255, 255, 255, 0.12);
  }

  .footer-bottom p {
    margin: 0;
    color: #aaa4bd;
    font-size: 0.82rem;
  }

  .footer-bottom a {
    display: grid;
    width: 38px;
    height: 38px;
    flex: 0 0 auto;
    place-items: center;
    border-radius: 9px;
    background: #ffc928;
    color: #130238;
  }

  .footer-bottom svg {
    width: 21px;
    height: 21px;
    fill: none;
    stroke: currentColor;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke-width: 2.5;
  }

  @media (max-width: 850px) {
    .footer-content {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    .footer-about {
      grid-column: 1 / -1;
    }
  }

  @media (max-width: 560px) {
    .footer-content {
      grid-template-columns: 1fr;
      width: min(100% - 32px, 1250px);
      padding: 52px 0 42px;
    }

    .footer-about {
      grid-column: auto;
    }

    .footer-bottom {
      width: min(100% - 32px, 1250px);
    }
  }
</style>
