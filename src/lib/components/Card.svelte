<script>
    export let titulo="Auto";
    export let descripcion="descripcion";
    export let img="#";
    export let precio="000.000";
    export let link = "#";
</script>



<style>
    .Card {
        background-color: var(--clear);
        width: 10rem;
        height: 13rem;
        padding: 0.6rem;
        border-radius: 0.4rem;
        box-shadow: 0px 0px 8px 1px rgba(0, 0, 0, 0.220);
        flex: none;
        display: flex;
        flex-direction: column;

        text-decoration: none;
        color: var(--dark);
        cursor: pointer;
    }
    
    .Card__img {
        width: 100%;
        height: 6rem;
        border-radius: 0.3rem 0.3rem 0 0;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: flex-end; 
    }
    
    img {
        height: 100%;
        max-width: none;
        width: auto;
    }

    .Card__text {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
        padding: 0.6rem 0;
    }

    .titulo {
        font-size: 0.9rem;
        font-weight: 700;
    }

    .descripcion {
        font-size: 0.65rem;
        font-weight: 300;
    }

    .precio {
        font-size: 0.85rem;
        font-weight: 400;
    }

    
    @media (min-width: 768px){
        .Card__text {
            gap: 0.6rem;
        }
    }
    
    @media (min-width: 768px){
        .Card {
            width: 12rem;
            height: 16rem;
        }

        .Card__img {
            height: 7.5rem;
        }

        .Card__text {
            gap: 0.7rem;
        }

    
        .titulo {
            font-size: 1rem;
        }

        .descripcion {
            font-size: 0.75rem;
        }

        .precio {
            font-size: 0.95rem;
        }
    }
    @media (min-width: 1024px){
        .Card {
            width: 14rem;
            height: 18rem;
        }

        .Card__img {
            height: 8.5rem;
        }

        .titulo {
            font-size: 1.1rem;
        }

        .descripcion{
            font-size: 0.85rem;
        }

        .precio {
            font-size: 1.05rem;
        }

    }
</style>



<a class="Card" id="" href={link} >
    <div class="Card__img"> 
        <img src="{img}" alt="">
    </div>
    <div class="Card__text">
        <h1 class="titulo">{titulo} </h1>
        <p class="descripcion">{descripcion}</p>
        <p class="precio">${precio}</p>
    </div>

</a>