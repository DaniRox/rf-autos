<script>
    
    import '../styles/reset.css';
    import '../styles/colors.css';
    import Home from "./Home/+page.svelte";
    
</script>

<style>

    @import url("https://use.typekit.net/dso2uji.css");
    :root{
        font-family: "petala-pro", sans-serif;
        
        font-size: 16px;
    }

    .main{
        width: 100%;
        height: auto;
        display: flex;
        flex-direction: column;
        position: relative;
        top: -0.1rem;
    }

</style>



<div class="main">
    <Home />
</div>