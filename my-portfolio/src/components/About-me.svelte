<script>
  import aboutImage from '../assets/weui--me-filled.png';
  import profilePhoto from '../assets/Indraneel.png';
  import profilePhotoColor from '../assets/Indraneel (color).jpeg';
</script>

<main id="about" class="about-section">
  <div class="about-heading">
    <img src={aboutImage} alt="" aria-hidden="true" />
    <h2>About <span>Me</span></h2>
  </div>

  <div class="about-content">
    <div class="about-photo">
      <img class="about-photo-base" src={profilePhoto} alt="Indraneel Chowdhury" />
      <img class="about-photo-color" src={profilePhotoColor} alt="" aria-hidden="true" />
    </div>

    <div class="my-description">
      <h3>I'm Indraneel</h3>
      <p class="role">Frontend Developer</p>
      <p>
        I am a frontend developer based in Assam, India, and an undergraduate
        student pursuing Electronics and Communication Engineering at
        North-Eastern Hill University. I am passionate about building responsive
        and user-friendly web applications while continuously learning and
        improving my development skills.
      </p>

      <p class="detail"><span>Email :</span> indraneelchowdhury1818@gmail.com</p>
      <p class="detail"><span>Place :</span> Assam, India</p>
    </div>
  </div>
</main>

<style>
  .about-section {
    padding: 72px 24px 88px;
    background: #ffffff;
    color: #17191f;
  }

  .about-heading {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 14px;
    margin: 0 auto;
    color: #202124;
  }

  .about-heading img {
    display: block;
    width: 46px;
    height: 46px;
    object-fit: contain;
  }

  .about-heading h2 {
    margin: 0;
    font-size: 50px;
    line-height: 1;
    font-weight: 900;
  }

  .about-heading span {
    color: #7c09bd;
  }

  .about-content {
    display: grid;
    grid-template-columns: minmax(280px, 390px) minmax(320px, 650px);
    align-items: center;
    justify-content: center;
    gap: 110px;
    width: min(1180px, 100%);
    margin: 96px auto 0;
  }

  .about-photo {
    position: relative;
    overflow: hidden;
    border-radius: 18px;
    background: #d8d8d8;
    box-shadow: 0 10px 24px rgba(0, 0, 0, 0.26);
    aspect-ratio: 0.75;
  }

  .about-photo img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: cover;
    filter: grayscale(1);
    transition: opacity 0.35s ease;
  }

  .about-photo .about-photo-color {
    position: absolute;
    inset: 0;
    opacity: 0;
    filter: none;
  }

  .about-photo:hover .about-photo-color {
    opacity: 1;
  }

  .my-description {
    max-width: 680px;
  }

  .my-description h3 {
    margin: 0;
    color: #202124;
    font-size: 40px;
    line-height: 1.1;
    font-weight: 900;
  }

  .role {
    margin: 9px 0 26px;
    color: #080443;
    font-size: 18px;
    font-weight: 800;
  }

  .my-description p {
    color: #050505;
    font-size: 17px;
    line-height: 1.55;
  }

  .detail {
    margin: 19px 0 0;
  }

  .detail span {
    color: #0647ff;
    font-weight: 700;
  }

  @media (max-width: 820px) {
    .about-content {
      grid-template-columns: 1fr;
      gap: 40px;
      margin-top: 56px;
    }

    .about-photo {
      width: min(360px, 100%);
      margin: 0 auto;
    }

    .my-description {
      margin: 0 auto;
      text-align: center;
    }
  }

  @media (max-width: 520px) {
    .about-section {
      padding: 56px 16px 72px;
    }

    .about-heading {
      gap: 9px;
    }

    .about-heading img {
      width: 38px;
      height: 38px;
    }

    .my-description p {
      font-size: 16px;
    }
  }
</style>
