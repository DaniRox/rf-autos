<script>
    import "../../../styles/reset.css";
    import "../../../styles/colors.css";
    import CarruselProducto from "$lib/components/CarruselProducto.svelte";
    import MiniaturaProducto from "$lib/components/MiniaturaProducto.svelte";

    export let fotoProducto="/img/auto3.jpg";
    export let titulo="Auto";
    export let precio="000.000";
    export let descripcion="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.";
    export let fotosMini=[ "/img/auto3.jpg" ];

    export let img1 = "/img/auto3.jpg";
    export let img2 = "/img/auto2.jpg";
    export let img3 = "/img/auto1.jpg"; 
    
    let images = [
        img1, 
        img2, 
        img3
    ];

</script>

<style>
    .cardProducto {
        width: 100%;
        height: auto;
        padding: 1.5rem 5%;
        display: flex;
        flex-direction: column;
    }

    .cardProducto-container{
        gap: 1.5rem;
        display: flex;
        flex-direction: column;
    }

    .tituloMovil{
        font-weight: 600;
        font-size: 1.7rem;
    }

    .tituloEscritorio{
        display: none;
        font-weight: 600;
        font-size: 2rem;
    }

    .fotosProducto{
        display: flex;
        flex-direction: column;
        align-items: center;
        height: 20rem;
    }

    .fotoPrincipal{
        display: none;
    }

    .carrouselproducto{
        display: flex;
        flex-direction: row;
        height: 100%;
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
        height: 100%;
    }

    img{
        height: 100%;
        max-width: none;
    }

    .infoProducto{
        padding: 1rem 0;
        display: flex;
        flex-direction: column;
        gap: 1rem;

    }

    .infoproducto-text{
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    .spanPrecio{
        font-weight: 400;
        font-size: 1.5rem;
    }

    .descripcion{
        font-weight: 300;
        font-size: 0.9rem;
        line-height: 110%;
    }
    
    .compra{
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    .cardProducto__caracteristicas {
        margin: 2rem 0;
    }

    .cardProducto__title {
        font-size: 1.2rem;
    }

    .caracteristicas-group {
        margin: 1.4rem 0;
    }

    .caracteristicas-group__title {
        font-size: 1rem;
    }

    table {
        width: 100%;
        margin: 0.5rem 0;
    }

    td {
        padding: 0.8rem;
        font-size: 0.8rem;
        font-weight: 300;
    }

    table tr td:first-child {
        font-weight: 500;
    }

    table tr:nth-child(even) {
        background-color: var(--celeste);
    }




    @media (min-width: 480px){
        .fotosProducto{
            height: 20rem;
        }
    }

    @media (min-width: 640px){
        .fotosProducto{
            height: 24rem;
        }
    }

    @media(min-width: 768px){
        .cardProducto-container{
            flex-direction: row;
        }

        .tituloMovil{
            display: none;
        }

        .tituloEscritorio{
            display: flex;
        }

        .fotosProducto{
            width: 50%; 
            height: 16rem; 
            display: flex;
            flex-direction: row;
            gap: 1rem;  
        }

        .fotoPrincipal{
            display: flex;
        }

        .carrouselproducto{
            display: none;
        }

        .infoProducto{
            padding: 0;
            gap: 2rem;
        }

        .miniaturas{
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            height: 100%;
            gap: 1rem;
        }

        .foto{
            width: 26rem;
        }

        .descripcion{
            font-size: 1rem;
        }
    }

    @media(min-width: 1024px){
        .fotosProducto{
            height: 20rem;
            width: auto;
            gap: 1rem;
        }
    }

</style>

<div class="cardProducto">
    <div class="cardProducto-container">
        <h1 class="tituloMovil">{titulo}</h1>
        <div class="fotosProducto">
            <div class="miniaturas">
            
                    {#each fotosMini as foto}
                        <MiniaturaProducto fotoMiniatura={foto} />
                    {/each}
            </div>

            <div class="foto"  >
                <img src={fotoProducto} alt="" class="fotoPrincipal">
                <div class="carrouselproducto">
                    <CarruselProducto
                        imagesProducto= {[img1,img2,img3]}
                    />
                </div>
            </div>
        </div>
        <div class="infoProducto">
            <div class="infoproducto-text">
                <h1 class="tituloEscritorio">{titulo}</h1>
                <p class="descripcion"> {descripcion}</p>
                
            </div>

            <div class="compra">
                <span class="spanPrecio">${precio}</span>

            </div>
        </div>
    </div>
    
    <div class="cardProducto__caracteristicas">
        <h2 class="cardProducto__title">Titulo</h2>

        <div class="caracteristicas-group">
            <h2 class="caracteristicas-group__title">subtitulo</h2>
            <table>
                <tbody>
                    <tr>
                        <td>caracteristica</td>
                        <td>caracteristica</td>
                    </tr>
                    <tr>
                        <td>caracteristica</td>
                        <td>caracteristica</td>
                    </tr>
                </tbody>
                
            </table>
        </div>

        <div class="caracteristicas-group">
            <h2>subtitulo</h2>
            <table>
                <tbody>
                    <tr>
                        <td>caracteristica</td>
                        <td>caracteristica</td>
                    </tr>
                    <tr>
                        <td>caracteristica</td>
                        <td>caracteristica</td>
                    </tr>
                </tbody>
                
            </table>
        </div>
    </div>
</div>