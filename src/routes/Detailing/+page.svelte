<script>
    import "../../styles/reset.css";
    import "../../styles/colors.css";
</script>

<style>
    .Servicios {
        width: 100%;
        min-height: 85vh;
        padding: 1rem 5%;
        gap: 1rem;
    }
    .Servicios__titles {
        color: var(--dark);
        padding: 1rem 0;
        display: flex;
        flex-direction: column;
        gap: 0.4rem;
    }

    .title {
        font-size: 1.8rem;
        font-weight: 900;
    }

    .subtitle {
        font-size: 1rem; 
        font-weight: 400;
    }

    .Servicios-container {
        padding: 1rem;
        display: flex;
        justify-content: center;
    }

    .Servicios__form {
        width: 25rem;
        background-color: var(--celeste);
        padding: 1.7rem;
        border-radius: 0.8rem;
        display: flex;
        flex-direction: column;
        gap: 1.2rem;
    }

    .form__group-input {
        display: flex;
        flex-direction: column;
        gap: 0.4rem;
    }

    label {
        color: var(--dark);
        font-size: 0.8rem;
        font-weight: 400;
    }

    .input {
        height: 2.4rem;
        padding: 0.2rem;
        border: 0.1rem solid var(--paynesGray);
        border-radius: 0.4rem;
        font-weight: 300;
        color: var(--dark);
    }

    textarea {
        height: 3rem;
    }

    .btn-form {
        background-color: var(--paynesGray);
        color: var(--clear);
        font-size: 0.8rem;
        font-weight: 400;
    }


    @media (min-width: 480px) {
        .title {
            font-size: 1.9rem; /* Ajustamos el tamaño para móviles */
        }

        .subtitle {
            font-size: 1.1rem; /* Ajustamos el tamaño para móviles */
        }
    }

    @media (min-width: 768px) {
        .Servicios__titles {
            gap: 0.6rem;
        }
        
        .title {
            font-size: 2rem; /* Ajustamos el tamaño para móviles */
        }

        .subtitle {
            font-size: 1.2rem; /* Ajustamos el tamaño para móviles */
        }

        .Servicios-container {
            padding: 1.5rem;
        }

        .Servicios__form {
            padding: 2rem;
        }

        .input {
            height: 2.6rem;
        }

        label {
            font-size: 0.9rem;
        }
    }

    @media (min-width: 1024px) {
        .title {
            font-size: 2.1rem; /* Ajustamos el tamaño para móviles */
        }

        .subtitle {
            font-size: 1.3rem; /* Ajustamos el tamaño para móviles */
        }

        .Servicios-container {
            padding: 2rem;
        }

    }


</style>



<div class="Servicios" id="Servicios">
    <div class="Servicios__titles">
        <h1 class="title">Tu vehiculo ideal te espera</h1>
        <h2 class="subtitle">Envia tu formulario y te enviamos el presupuesto</h2>
    </div>

    <div class="Servicios-container">
        <form action="" class="Servicios__form">
            <div class="form__group-input">
                <label for="">Nombre</label>
                <input type="text" class="input">
            </div>

            <div class="form__group-input">
                <label for="">Apellido</label>
                <input type="text" class="input">
            </div>

            <div class="form__group-input">
                <label for="">Email</label>
                <input type="text" class="input">
            </div>

            <div class="form__group-input">
                <label for="">Número de teléfono</label>
                <input type="text" class="input">
            </div>

            <div class="form__group-input">
                <label for="">Marca, modelo y año</label>
                <input type="text" class="input">
            </div>

            <div class="form__group-input">
                <label for="">Descripcion del trabajo a realizar</label>
                <textarea name="" id="" class="input" placeholder="placeholder"></textarea>
            </div>

            <div class="form__group-input">
                <input type="submit" value="Enviar" class="input btn-form">
            </div>
            
        </form>
    </div>

</div>