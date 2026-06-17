<script>
    let isMenuOpen = false;

    function toggleMenu() {
        isMenuOpen = !isMenuOpen;
    }

    function closeMenu() {
        isMenuOpen = false;
    }
</script>

<nav aria-label="Primary navigation">
    <a class="brand" href="#home" aria-label="Indraneel home">
        <span class="brand-mark">I</span>
        <span>Indraneel</span>
    </a>

    <button 
        class="hamburger" 
        aria-label="Toggle navigation menu" 
        aria-expanded={isMenuOpen}
        on:click={toggleMenu}
    >
        <span class="hamburger-line"></span>
        <span class="hamburger-line"></span>
        <span class="hamburger-line"></span>
    </button>

    <div class="nav-links" class:open={isMenuOpen}>
        <a class="active" href="#home" on:click={closeMenu}>Home</a>
        <a href="#about" on:click={closeMenu}>About</a>
        <a href="#skills" on:click={closeMenu}>Skills</a>
        <a href="#education" on:click={closeMenu}>Education</a>
        <a href="#projects" on:click={closeMenu}>Projects</a>
        <a href="#experience" on:click={closeMenu}>Experience</a>
        <a href="#contact" on:click={closeMenu}>Contact</a>
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

    .hamburger {
        display: none;
        flex-direction: column;
        gap: 0.35rem;
        background: none;
        border: none;
        cursor: pointer;
        padding: 0.5rem;
        position: relative;
        z-index: 11;
    }

    .hamburger-line {
        display: block;
        width: 28px;
        height: 3px;
        background: #061f55;
        border-radius: 2px;
        transition: all 0.3s ease;
    }

    @media (max-width: 980px) {
        nav {
            align-items: center;
            flex-direction: row;
            gap: 0.9rem;
            min-height: auto;
            padding-block: 1rem;
            justify-content: space-between;
        }

        .hamburger {
            display: flex;
        }

        .nav-links {
            position: absolute;
            top: 78px;
            left: 0;
            right: 0;
            flex-direction: column;
            gap: 0.5rem;
            background: rgba(255, 255, 255, 0.98);
            backdrop-filter: blur(14px);
            border-bottom: 1px solid rgba(6, 31, 85, 0.08);
            padding: 1rem;
            max-height: 0;
            overflow: hidden;
            opacity: 0;
            transition: max-height 0.3s ease, opacity 0.3s ease;
            width: 100%;
            justify-content: flex-start;
        }

        .nav-links.open {
            max-height: 500px;
            opacity: 1;
            padding: 1rem;
        }

        .nav-links a {
            padding: 0.7rem 1rem;
            border-radius: 6px;
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
            top: 72px;
            padding: 0.75rem;
        }

        .nav-links.open {
            max-height: 400px;
            padding: 0.75rem;
        }

        .nav-links a {
            font-size: 0.9rem;
            padding: 0.55rem 0.7rem;
        }

        .hamburger-line {
            width: 24px;
            height: 2.5px;
        }
    }
</style>
