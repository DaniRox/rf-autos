<script>
    export let img1 = "/img/autos.jpg";
    export let img2 = "/img/seguros.jpg";
    export let img3 = "/img/detailing.jpg"; 

    let images = [
        img1, 
        img2, 
        img3
    ];

    let currentImageIndex = 0; 

    function nextImage() {
        currentImageIndex = (currentImageIndex + 1) % images.length;
    }

    function prevImage() {
        currentImageIndex = (currentImageIndex - 1 + images.length) % images.length;
    }

    let intervalId =0;  

    function startAutoSlide() {
        intervalId = setInterval(nextImage, 3000);
    }

    function stopAutoSlide() {
        clearInterval(intervalId);
    }

    startAutoSlide();
</script>



<style>
    .Carrusel { 
        position: relative; 
        width: 100%;
        height: 11rem;
        margin: 0 auto; 
        overflow: hidden;
    }

    .Carrusel::after {
        content: '';
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        height: 4rem; /* Altura del efecto difuminado */
        background: linear-gradient(to bottom, rgba(255, 255, 255, 0), rgba(255, 255, 255, 1)); /* Gradiente blanco */
        pointer-events: none; /* Asegura que no interfiera con los clics */
        z-index: 2; /* Coloca el efecto encima del contenido */
    }

    .Carrusel__image-container { 
        display: flex;
        align-items: center;
        transition: transform 0.8s ease; 
        width: 100%;
        height: 100%;
    } 

    .image-wrapper { 
        min-width: 100%;
    } 

    .image-wrapper img {
        width: 100%; 
        height: auto;
        object-fit: cover;
        object-position: center; 
    } 

    .Carrusel__arrows-container { 
        position: absolute; 
        top: 50%; 
        transform: translateY(-50%); 
        display: flex; 
        justify-content: space-between; 
        width: 100%; 
    }

    .arrows-container__arrow { 
        background-color: transparent; 
        border: none; 
        font-size: 1rem; 
        cursor: pointer; 
        padding: 0rem; 
    } 

    .arrows-container__arrow--left { 
        left: 0;
        transform: rotate(90deg);
    } 

    .arrows-container__arrow--right { 
        right: 0;
        transform: rotate(270deg);
    }

    .flechaicono{
        width: 1.7rem;
    }




    @media (min-width: 480px){
        .Carrusel { 
            width: 100%;
            height: 15rem;
        }
    }

    @media (min-width: 768px){
        .Carrusel { 
            width: 100%;
            height: 18rem;
        }

        .flechaicono { 
            width : 3rem; 
        }
    }

    @media (min-width: 1024px){
        .Carrusel { 
            width: 100%;
            height: 23rem;
        }

        .flechaicono { 
            width : 4rem; 
        }
    }
</style>



<div class="Carrusel">
    <div class="Carrusel__image-container" style="transform: translateX({-currentImageIndex * 100}%)"> 
        {#each images as image} 
            <div class="image-wrapper">
                <img src={image} alt="Carrusel Imagen" />
            </div> 
        {/each}
    </div>

    <div class="Carrusel__arrows-container"> 
        <button class="arrows-container__arrow arrows-container__arrow--left" on:click={prevImage}><img class="flechaicono"  src="/img/flechaicono.svg" alt=""> </button> 
        <button class="arrows-container__arrow arrows-container__arrow--right" on:click={nextImage}><img class="flechaicono" src="/img/flechaicono.svg" alt=""></button>
    </div>
</div>