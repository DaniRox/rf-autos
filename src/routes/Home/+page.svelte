<script>
    import "../../styles/reset.css";
    import "../../styles/colors.css";
    import Banner from "$lib/components/Banner.svelte";
    import Container from "$lib/components/Container.svelte";
    import Card from "$lib/components/Card.svelte";
	import Carrusel from "$lib/components/Carrusel.svelte";
    
</script>



<style>
    .Home{
        width: 100%;
        height: auto;
        min-height: 85vh;
        padding-bottom: 1rem;
    }

    .Home-container {
        height: auto;
        display: flex;
        flex-direction: column;
        padding: 1rem 5%;
        gap: 1rem;
    }

    .banner-container {
        width: 100%;
        display: flex;
        flex-direction: row;
        gap: 1rem;
    }
    

    @media (min-width: 480px) {
        .Home-container {
            gap: 1.5rem;
        }

        .banner-container {
            gap: 1.5rem;
        }
    }

    @media (min-width: 768px) {
        .Home {
            padding-bottom: 1.5rem;
        }

        .Home-container {
            padding: 1.5rem 5%;
        }

        .banner-container {
            gap: 1.7rem;
        }
    }

    @media (min-width: 1024px) {
        .Home {
            padding-bottom: 2rem;
        }

        .Home-container {
            padding: 1.5rem 5%;
        }

        .banner-container {
            gap: 2rem;
        }
    }
</style>



<main class="Home" id="Inicio">

    <Carrusel/>

    <div class="Home-container">

        <Banner 
            h2="Encontra lo que buscas"
            h1="Vehiculos"
            img="/img/autos.jpg"
            link="../Vehiculos/"
            heightLg="15rem"
        />

        <div class="banner-container">
            <Banner
                h2="Que buscas?"
                h1="Detailing"
                img="/img/detailing.jpg"
                link="../Detailing/"
                heightLg="15rem"
            />

            <Banner
                h2="Cotiza hoy mismo"
                h1="Seguros"
                img="/img/seguros.jpg"
                link="../Seguros/"
                heightLg="15rem"
            />
        </div>

        <Banner 
            h2="Encontra lo que buscas"
            h1="Vende"
            img="/img/venta.jpg"
            link="../Vende/"
            heightLg="15rem"
        />

    </div>
    
    <div class="Home-container">
        <Container> 
            <Card
                img="/img/auto1.jpg"
                descripcion="Cotiza tu seguro y busca el mejor precio."
                link="../Vehiculos/Vehiculo/"
            />

            <Card
                img="/img/auto2.jpg"
                descripcion="Cotiza tu seguro y busca el mejor precio."
                link="../Vehiculos/Vehiculo/"
            />

            <Card
                img="/img/auto3.jpg"
                descripcion="Cotiza tu seguro y busca el mejor precio."
                link="../Vehiculos/Vehiculo/"
            />

            <Card
                img="/img/auto4.jpg"
                descripcion="Encontra el vehiculo perfecto para vos"
                link="../Vehiculos/Vehiculo/"
            />

            <Card
                img="/img/auto1.jpg"
                descripcion="Plantin de tomate cherry 10cm alto"
                link="../Vehiculos/Vehiculo/"
            />

            <Card
                img="/img/auto2.jpg"
                descripcion="Plantin de tomate cherry 10cm alto"
                link="../Vehiculos/Vehiculo/"
            />

        </Container>
    </div>
    
</div>
