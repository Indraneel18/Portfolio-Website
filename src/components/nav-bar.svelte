<nav aria-label="Primary navigation">
    <a class="brand" href="#home" aria-label="Indraneel home">
        <span class="brand-mark">I</span>
        <span>Indraneel</span>
    </a>

    <div class="nav-links">
        <a class="active" href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#education">Education</a>
        <a href="#projects">Projects</a>
        <a href="#experience">Experience</a>
        <a href="#contact">Contact</a>
    </div>
</nav>

<style>
    nav {
        align-items: center;
        background: rgba(255, 255, 255, 0.94);
        backdrop-filter: blur(14px);
        border-bottom: 1px solid rgba(6, 31, 85, 0.08);
        box-shadow: 0 12px 30px rgba(6, 31, 85, 0.12);
        color: #061f55;
        display: flex;
        gap: 2rem;
        justify-content: space-between;
        min-height: 78px;
        padding: 0 clamp(1.5rem, 5vw, 5.6rem);
        position: relative;
        z-index: 10;
    }

    .brand {
        align-items: center;
        color: inherit;
        display: inline-flex;
        flex: 0 0 auto;
        gap: 0.75rem;
        font-size: 1.5rem;
        font-weight: 900;
        letter-spacing: 0;
        text-decoration: none;
    }

    .brand-mark {
        display: inline-grid;
        width: 42px;
        height: 42px;
        place-items: center;
        border-radius: 50%;
        background: #ffc700;
        box-shadow: 0 10px 20px rgba(255, 199, 0, 0.28);
        color: #061f55;
        font-size: 1.2rem;
    }

    .nav-links {
        align-items: center;
        display: flex;
        flex-wrap: wrap;
        gap: 0.25rem;
        justify-content: flex-end;
    }

    .nav-links a {
        border-radius: 999px;
        color: #061f55;
        font-size: 1rem;
        font-weight: 800;
        padding: 0.7rem 0.95rem;
        position: relative;
        text-decoration: none;
        transition: background 0.2s ease, color 0.2s ease, transform 0.2s ease;
    }

    .nav-links a:hover,
    .nav-links a.active {
        background: rgba(255, 199, 0, 0.24);
        color: #ff7300;
        transform: translateY(-1px);
    }

    .nav-links a::after {
        position: absolute;
        right: 1rem;
        bottom: 0.35rem;
        left: 1rem;
        height: 2px;
        border-radius: 999px;
        background: #ff7300;
        content: '';
        opacity: 0;
        transform: scaleX(0.5);
        transition: opacity 0.2s ease, transform 0.2s ease;
    }

    .nav-links a:hover::after,
    .nav-links a.active::after {
        opacity: 1;
        transform: scaleX(1);
    }

    @media (max-width: 980px) {
        nav {
            align-items: flex-start;
            flex-direction: column;
            gap: 0.9rem;
            min-height: auto;
            padding-block: 1rem;
        }

        .nav-links {
            justify-content: flex-start;
            width: 100%;
        }
    }

    @media (max-width: 560px) {
        nav {
            padding-inline: 1rem;
        }

        .brand {
            font-size: 1.25rem;
        }

        .brand-mark {
            width: 38px;
            height: 38px;
        }

        .nav-links {
            gap: 0.15rem;
        }

        .nav-links a {
            font-size: 0.9rem;
            padding: 0.55rem 0.7rem;
        }
    }
</style>
