<script>
    import "../../../styles/reset.css";
    import "../../../styles/colors.css";
</script>

<style>
    .Seguros-auto {
        width: 100%;
        min-height: 85vh;
        padding: 1rem 5%;
        gap: 1rem;
    }
    .Seguros-auto__titles {
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

    .Seguros-auto-container {
        padding: 1rem;
        display: flex;
        justify-content: center;
    }

    .Seguros-auto__form {
        width: 25rem;
        background-color: var(--atomicTangerine);
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
        color: var(--honeydew);
        font-size: 0.8rem;
        font-weight: 400;
    }

    .input {
        height: 2.4rem;
        padding: 0.2rem;
        border: 0.1rem solid var(--honeydew);
        border-radius: 0.4rem;
    }

    textarea {
        height: 3rem;
    }

    .btn-form {
        background-color: var(--honeydew);
        color: var(--atomicTangerine);
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
        .Seguros-auto__titles {
            gap: 0.6rem;
        }
        
        .title {
            font-size: 2rem; /* Ajustamos el tamaño para móviles */
        }

        .subtitle {
            font-size: 1.2rem; /* Ajustamos el tamaño para móviles */
        }

        .Seguros-auto-container {
            padding: 1.5rem;
        }

        .Seguros-auto__form {
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

        .Seguros-auto-container {
            padding: 2rem;
        }

    }


</style>

<div class="Seguros-auto" id="Seguros-auto">
    <div class="Seguros-auto__titles">
        <h1 class="title">El seguro para tu auto</h1>
        <h2 class="subtitle">Envia tu formulario y te enviamos el presupuesto</h2>
    </div>

    <div class="Seguros-auto-container">
        <form action="" class="Seguros-auto__form">
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
                <label for="">Marca del auto</label>
                <input type="text" class="input">
            </div>

            <div class="form__group-input">
                <label for="">Modelo del auto</label>
                <input type="text" class="input">
            </div>

            <div class="form__group-input">
                <label for="">Año del auto</label>
                <input type="text" class="input">
            </div>

            <div class="form__group-input">
                <label for="">Fotos</label>
                <input type="text" class="input">
            </div>

            <div class="form__group-input">
                <label for="">Comentarios</label>
                <textarea name="" id="" class="input"></textarea>
            </div>

            <div class="form__group-input">
                <input type="submit" value="Enviar" class="input btn-form">
            </div>
            
        </form>
    </div>

</div>