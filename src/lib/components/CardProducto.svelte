<script>
    export let fotoProducto="#";
    export let titulo="titulo";
    export let precio="precioUnitario";
    export let descripcion="descrpion";
    export let stock="1";
    export let cantidad="00";
</script>

<style>
    .cardProducto{
        width: 100%;
        padding: 1rem;
        gap: 2rem;
        display: flex;
        flex-direction: column;
    }
    .tituloMovil{
        font-weight: 500;
        font-size: 1.2rem;
    }
    .tituloEscritorio{
        display: none;
    }
    .fotosProducto{
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .miniaturas{
        display: none;
    }
    .foto{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: flex-end;
        overflow: hidden;
        height: 16rem;
    }
    img{
        height: 100%;
        max-width: none;
    }
    .infoProducto{
        display: flex;
        flex-direction: column;
        gap: 0.6rem;

    }
    .spanPrecio{
        font-weight: 400;
        font-size: 1.6rem;
    }
    .descripcion{
        font-weight: 300;
        font-size: 0.9rem;
    }
    .spanUnidades{
        font-weight: 600;
        font-size: 0.8rem;
        color: var(--plant);
    }



</style>

<div class="cardProducto">
    <h1 class="tituloMovil">{titulo}</h1>
    <div class="fotosProducto">
        <div class="miniaturas"></div>
        <div class="foto"  >
            <img src={fotoProducto} alt="">
        </div>
    </div>
    <div class="infoProducto">
        <h1 class="tituloEscritorio">{titulo}</h1>
        <span class="spanPrecio">${precio}</span>
        <p class="descripcion"> {descripcion}</p>

        <div class="compra">
            <span class="spanUnidades">{stock} Disponible</span>
            <div class="botones">
                <div class="cantidad">
                    <button ><img src="/img/BiDash.svg" alt=""></button>
                    <span class="spanCantidad">{cantidad}</span>
                    <button><img src="/img/BiPlus.svg" alt=""></button>
                </div>
                <button class= "carrito">Agregar al carrito</button>
            </div>
        </div>
    </div>
    
</div>