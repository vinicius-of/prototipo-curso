<script>
    import Profile from './Profile.svelte'
</script>

<main>
    <h1>Time</h1>
    <ul>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
    </ul>
</main>
<style>
    main {
        width: 100%;
        background-color: #e84b60;
        margin: 30px 0;
    }

    h1 {
        color: white;
        text-align: center;
        margin: 0;
        padding: 30px 0;
    }

    ul {
        display: flex;
        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;
        max-width: 1195px;

        display: -webkit-flex;
        display: -ms-flexbox;
        -ms-flex-wrap: wrap;

        padding: 0;
        margin: 0 auto;
    }

    li {
        list-style: none;
        padding: 0 50px;

    }
</style>