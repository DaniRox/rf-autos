<script>
    import { onMount } from 'svelte';
    let showMenu = false;
    let isMobile = true;

    function closeMenu() {
        if (isMobile) {
            showMenu = false;
        }
    }

    function toggleMenu() {
        if (isMobile) {
            showMenu = !showMenu;
        }
    }

    function handleResize() {
        if (window.innerWidth >= 768) {
            isMobile = false;
            showMenu = true;
        } else {
            isMobile = true;
            showMenu = false;
        }
    }

    onMount(() => {
        handleResize();
        window.addEventListener('resize', handleResize);
        return () => window.removeEventListener('resize', handleResize);
    });

    function smoothScroll(event) {
        event.preventDefault();
        const targetId = event.currentTarget.getAttribute("href").substring(1);
        const targetElement = document.getElementById(targetId);
        targetElement.scrollIntoView({ behavior: "smooth" });
    }
</script>

<style>
    .Navbar {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        background-color: var(--paynesGray);
        padding: 0.8rem 5%;
    }

    .Navbar__menu-navbar {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    .menu-navbar__logo {
        font-size: 1.5rem;
        color: #ffffff;
        font-family: "Dating";
        font-weight: 800;
    }

    .menu-navbar__buscador {
        width: 12rem;
        height: 2.3rem;
        background-color: var(--clear);
        display: flex;
        flex-direction: row;
        align-items: center;
        border-radius: 0.2rem;
        padding: 0.2rem;
    }

    .buscador__input-text {
        width: 100%;
        border: none;
        font-size: 1rem;
        font-weight: 300;
        color: var(--black);
        padding: 0 0.5rem;
        background-color: transparent;
    }

    .buscador__btn-lupa {
        width: 1.8rem;
        cursor: pointer;
        border: none;
        padding: 0.2rem;
    }

    .buscador__icon-lupa {
        width: 100%;
        height: auto;
    }

    .menu-navbar__buttons {
        display: flex;
        flex-direction: row;
        gap: 1rem;
    }

    .menu-navbar__user-btn {
        border: none;
        cursor: pointer;
    }

    .menu-navbar__user-btn-icon {
        width: 1.5rem;
    }

    .menu-navbar__menu-mobile {
        border: none;
        cursor: pointer;
    }

    .menu-navbar__icon-menu {
        height: 1.5rem;
    }

    .Navbar__navlinks {
    }

    .navlinks__menu-links {
        width: 100%;
        background-color: var(--paynesGray);
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        position: absolute;
        padding: 1rem 5% 1rem 0;
        left: 0;
        top: 3rem;
        z-index: 5;
    }

    .text {
        padding: 0.7rem 0;
        cursor: pointer;
        transition: all 0.3s ease;
        color: var(--clear);
        font-size: 0.8rem;
        font-weight: 500;
    }

    .text:hover {
        color: var(--celeste);
        transform: scale(1.05, 1.05);
    }

    .link {
        text-decoration: none;
        color: inherit;
    }


    @media (min-width: 480px) {
        .menu-navbar__buscador {
            width: 18rem;
        }
    }
    
    @media (min-width: 768px) {
        .Navbar {
            padding: 1rem 5%;
            flex-direction: column;
            gap: 0.5rem;
        }

        .menu-navbar__buttons {
            gap: 0rem;
        }

        .menu-navbar__buscador {
            width: 75%;
        }

        .menu-navbar__icon-menu {
            display: none;
        }

        .Navbar__navlinks {
            width: 100%;
            position: relative;
            justify-content: center;
            display: flex;
            flex-direction: row;
        }

        .navlinks__menu-links {
            position: relative;
            align-items: center;
            width: auto;
            flex-direction: row;
            padding: 0;
            top: 0;
            gap: 2.6rem;
        }

        .text {
            font-size: 0.9rem;
        }

    }
    @media (min-width: 1024px) {
        .Navbar {
            padding: 1rem 5%;
            gap: 0.5rem;
        }

        .text {
            font-size: 1rem;
        }

    }
</style>

<nav class="Navbar">
    <div class="Navbar__menu-navbar">

        <p class="menu-navbar__logo">RFyS</p>

        <div class="menu-navbar__buscador">
            <input type="text" class="buscador__input-text"> 
            <button class="buscador__btn-lupa">
                <img src="/img/search.png" alt="Buscar" class="buscador__icon-lupa">
            </button> 
        </div>

        <div class="menu-navbar__buttons">
            <button class="menu-navbar__user-btn">
                <img src="/img/user.png" alt="" class="menu-navbar__user-btn-icon">
            </button>

            <button on:click={toggleMenu} class="menu-navbar__menu-mobile">
                <img src="/img/menu.png" alt="menu" class="menu-navbar__icon-menu" >
            </button>

        </div>
        
        
    </div>

    <div class="Navbar__navlinks">
        {#if showMenu || !isMobile}
            <ul class="navlinks__menu-links">
                <li class="text"><a href="/" class="link" on:click={closeMenu}>Inicio</a></li>
                <li class="text"><a href="/Vehiculos" class="link" on:click={closeMenu}>Vehiculos</a></li>
                <li class="text"><a href="/Seguros" class="link" on:click={closeMenu}>Seguros</a></li>
                <li class="text"><a href="/Detailing" class="link" on:click={closeMenu}>Detailing</a></li>
                <li class="text"><a href="/Vende" class="link" on:click={closeMenu}>Vende tu auto</a></li>
            </ul>
        {/if}

    </div>
        
</nav>
