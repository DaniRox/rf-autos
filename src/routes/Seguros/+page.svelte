<script>
    import "../../styles/reset.css";
    import "../../styles/colors.css";
	import Banner from "$lib/components/Banner.svelte";
    
</script>



<style>
    .Seguros {
        width: 100%;
        min-height: 85vh;
        padding: 1rem 5%;
        gap: 1rem;
    }

    .Seguros__titles {
        color: var(--dark);
        padding: 1rem 0;
        display: flex;
        flex-direction: column;
        gap: 0.4rem;
    }

    .title {
        font-size: 1.8rem;
        font-weight: 900;
    }

    .subtitle {
        font-size: 1rem; 
        font-weight: 400;
    }

    .banner-container {
        width: 100%;
        display: flex;
        padding: 1rem 0;
        flex-direction: column;
        gap: 1rem;
    }

    @media (min-width: 480px) {
        .title {
            font-size: 1.9rem; /* Ajustamos el tamaño para móviles */
        }

        .subtitle {
            font-size: 1.1rem; /* Ajustamos el tamaño para móviles */
        }
    }

    @media (min-width: 768px) {
        .banner-container {
            width: 100%;
            display: flex;
            flex-direction: row;
            gap: 1rem;
        }

        .Seguros__titles {
            gap: 0.6rem;
        }
        
        .title {
            font-size: 2rem; /* Ajustamos el tamaño para móviles */
        }

        .subtitle {
            font-size: 1.2rem; /* Ajustamos el tamaño para móviles */
        }
    }

    @media (min-width: 1024px) {
        .title {
            font-size: 2.1rem; /* Ajustamos el tamaño para móviles */
        }

        .subtitle {
            font-size: 1.3rem; /* Ajustamos el tamaño para móviles */
        }
    }
</style>



<div class="Seguros">
    <div class="Seguros__titles">
        <h1 class="title">Pedi tu presupuesto.</h1>
        <h2 class="subtitle">Mejoramos cualquier precio.</h2>
    </div>

    <div class="banner-container">
        <Banner
            h2="Envia tu informacion y pedi presupuesto"
            h1="Autos"
            img="/img/auto.jpg"
            link="../Seguros/auto"
            backgroundColor="rgba(238, 150, 96, 0.5)"
            hoverBackgroundColor="rgba(238, 150, 96, 0.8)"
            heightMg="18rem"
            heightLg="22rem"

        />

        <Banner
            h2="Envia tu informacion y pedi presupuesto"
            h1="Motos"
            img="/img/moto.jpg"
            link="../Seguros/moto"
            backgroundColor="rgba(238, 150, 96, 0.5)"
            hoverBackgroundColor="rgba(238, 150, 96, 0.8)"
            heightMg="18rem"
            heightLg="22rem"
        />
    </div>

</div>