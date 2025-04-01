<script>
    import "../../styles/reset.css";
    import "../../styles/colors.css";
    export let fotoMiniatura = "#"
    

</script>
<style> 
    .MiniaturaProducto{
        width: 2.5rem;
        height: 2.5rem;
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: flex-end;
    }
    img{
        height: 100%;
        width: auto;
        max-width: none;

    }
    @media(min-width: 1024px){
        .MiniaturaProducto{
            height: 4rem;
            width: 4rem;
        }
}


</style>

<div class="MiniaturaProducto">
    <img src={fotoMiniatura} alt="">
</div>