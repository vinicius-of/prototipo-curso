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

    img {
        width: 200px;
        border-radius: 100%;
    }

    .profile {
        text-align: center;
        margin-bottom: 30px;
    }
</style>