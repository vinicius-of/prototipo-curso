<script>
    export let name;
    export let title;
    export let image;
</script>

<main>
    <div class="profile">
        <img src="./assets/placeholder-perfil.jpg" alt={"Imagem de perfil do " + name}>
        <h2>Barros</h2>
        <p>Professor Dr. Ufal</p>
    </div>
</main>

<style>

    * {
        color: white;
        margin: 0;
        padding: 0;
    }

    h2 {
        font-style: normal;
        font-weight: 900;
        font-size: 48px;
        line-height: 58px;
    }

    p {
        font-style: normal;
        font-weight: normal;
        font-size: 30px;
        line-height: 36px;
    }

    img {
        width: 309.76px;
        height: 309.76px;
        border-radius: 100%;
        background-blend-mode: normal;
    }

    .profile {
        text-align: center;
        margin-bottom: 30px;
    }
</style>