<script>
    
</script>



<style>
    .Container {
        width: 100%;
        height: auto;
        display: flex;
        flex-direction: row;
        padding: 1rem 0 1rem 0.25rem;
        gap: 1.5rem;
        overflow-x: auto; 
        scroll-behavior: smooth;
    }

    .Container::-webkit-scrollbar {
        display: none;
    }
    
    .Container {
        scrollbar-width: none;
    }

    @media(min-width:480px){
    }

    @media(min-width:768px){
        .Container {
            gap: 1.7rem;
        }
    }

    @media(min-width:1024px){
        .Container {
            gap: 2rem;
        }
    }
</style>



<div class="Container">
    <slot><!-- optional fallback --></slot>
</div>