<script>
    import "../../styles/reset.css";
    import "../../styles/colors.css";
	import Container from './Container.svelte';
    export let imagesProducto = [  ];    
    let currentImageIndex = 0; 
    let container;
    
    function updateCurrentIndex() {
        if (!container) return;
        const scrollLeft = container.scrollLeft;
        const width = container.clientWidth;
        currentImageIndex = Math.round(scrollLeft / width);
    }
    function scrollToImage(index) {
        if (!container) return;
        const width = container.clientWidth;
        container.scrollTo({ left: index * width, behavior: "smooth" });
    }

</script>
    


<style>
    .carrusel { 
        width: 100%;
        height: 100%;
    }

    .image-container { 
        display: flex; 
        width: 100%;
        height: 100%;
        gap: 2rem;
        margin: 0 auto; 
        overflow-x: auto;
        position: relative; 
        scroll-snap-type: x mandatory;
        scroll-behavior: smooth;
        -webkit-overflow-scrolling: touch;
    } 

    .image-wrapper { 
        min-width: 100%;
        display: flex;
        align-items: flex-end;
        scroll-snap-align: center;
        overflow: hidden;
    }

    .image-wrapper img {
        width: 100%; 
        height: 100%;
        object-fit: cover; 
    }

    .dots{
        position: absolute;
        display: flex;
        flex-direction: row;
        padding: 1rem 0;
        left: 45%;
        gap: 0.5rem;

    }

    .dot{
        width: 0.6rem;
        height: 0.6rem;
        border-radius: 50%;
        background-color: #c8c8c8;
    }
    .dot.active{
        background-color:var(--newGrowph);
    }
    @media (min-width:480px){
        
    }


</style>



<div class="carrusel">
    {#if imagesProducto.length > 0}
    <div class="image-container" bind:this={container} on:scroll={updateCurrentIndex}> 
        {#each imagesProducto as image} 
            <div class="image-wrapper">
                <img src={image} alt="Carrusel Image" />
            </div> 
        {/each}
    </div> 
    <div class="dots">
        {#each imagesProducto as _, index} 
        <div class="dot {index === currentImageIndex ? 'active' : ''}" on:click={() => scrollToImage(index)}>
        </div> 
        {/each}
    </div>
    {:else}
    <p style="text-align: center; padding: 1rem;">
        No hay imagenes disponibles
    </p>      
    {/if}

</div>