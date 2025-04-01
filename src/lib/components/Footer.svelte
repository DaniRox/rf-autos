<script>

</script>

<style>
    .Footer{
        background-color: var(--dark);
        width: 100%;
        height: auto;
        font-size: 0.8rem;
        color: var(--celeste);
        font-weight: 300;
        padding: 1.5rem 5%;
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    a {
        text-decoration: none;
        font-size: 0.8rem;
        font-weight: 400;
    }

    a:hover {
        color: var(--celeste);
    }

    @media(min-width: 768px){
        .Footer{
            padding: 2rem 5%;
            flex-direction: row;
            justify-content: space-between;
        }

        a {
            font-size: 0.9rem;
        }
    }

    @media(min-width: 1024px){
        .Footer{
            padding: 3rem 5%;
            flex-direction: row;
            justify-content: space-around;
        }   
    }
</style>


<div class="Footer">
    <a href="mailto:RFyS@rapidofacilyseguro.com">RFyS@rapidofacilyseguro.com </a>
    <a href="/Sobrenosotros">Sobre nosotros</a>

</div>