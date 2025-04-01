<script>    
    export let h2="h2";
    export let h1="h1";
    export let img="#";

    // Propiedades opcionales
    export let link = "";      // Vacío por defecto, se asume que no se provee
    export let onClick = null; // null por defecto, se asume que no se provee

    export let backgroundColor = "rgba(179, 242, 221, 0.5)";
    export let hoverBackgroundColor = "rgba(179, 242, 221, 0.8)";

    // Propiedad para la altura en pantallas >= 768px
    export let heightMd = null;
    export let heightLg = null;
</script>



<style>
    a, .Banner {
        width: 100%;
        height: 7rem;
        border-radius: 0.4rem;
        box-sizing: border-box;
        display: flex;
        justify-content: center;
        align-items: center;
        overflow: hidden;
        transition: all 0.50s;
    }

    .Banner:hover {
        background-color: var(--banner-hover-bg-color, rgba(179, 242, 221, 0.8));
    }

    .Banner__text {
        color: var(--dark);
        position: absolute;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        z-index: 5;
    }

    .text__h2 {
        font-size: 0.8rem;
        font-weight: 700;
    }

    .text__h1 {
        font-size: 1.8rem;
        font-weight: 700;
        text-transform: uppercase;
    }

    .Banner__img {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: flex-end;
    }

    img{
        max-width: none;
        width: 100%;
        z-index: -1;
    }


    @media(min-width: 480px) {
        a, .Banner {
            height: 7.5rem;
        }
    }

    @media(min-width: 768px) {
        a, .Banner {
            height: var(--banner-height-md);
        }


        .text__h2 {
            font-size: 0.9rem;
        }

        .text__h1 {
            font-size: 2rem;
        }
    }

    @media(min-width: 1024px) {
        a, .Banner {
            height: var(--banner-height-lg);
        }

        .text__h2 {
            font-size: 1rem;
        }

        .text__h1 {
            font-size: 2.4rem;
        }

        .Banner__img {
            height: 100%;
        }
    }
</style>



{#if link}
    <!-- Si se proporciona 'link', envolvemos el banner en un enlace.
        Si se proporciona 'onClick', lo asignamos al enlace. -->
    <a href={link} class:hover={true} style="background-color: {backgroundColor}; --banner-hover-bg-color: {hoverBackgroundColor}; --banner-height-lg: {heightLg};" on:click={onClick}>
        <div class="Banner">
            <div class="Banner__text">
                <p class="text__h2">{h2}</p>
                <p class="text__h1">{h1}</p>
            </div>
            <div class="Banner__img"> 
                <img src={img} alt="">
            </div>
        </div>
    </a>
{:else}
    <!-- Si no hay link, asignamos el onClick directamente al contenedor -->
    <div class="Banner" class:hover={true} style="background-color: {backgroundColor}; --banner-hover-bg-color: {hoverBackgroundColor}; --banner-height-lg: {heightLg};" on:click={onClick}>
        <div class="Banner__text">
            <p class="text__h2">{h2}</p>
            <p class="text__h1">{h1}</p>
        </div>
        <div class="Banner__img"> 
            <img src={img} alt="">
        </div>
    </div>
{/if}