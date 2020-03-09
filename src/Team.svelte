<script>
    import Profile from './Profile.svelte'
</script>

<main>
    <h1>Time</h1>
    <ul class="team-list">
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
        margin: 75px 0;
    }

    h1 {
        color: white;
        text-align: center;

        font-weight: 900;
        font-size: 72px;
        line-height: 86px;

        margin: 0;
        padding: 89px 0;
    }

    .team-list {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        max-width: 1278.99px;

        display: -webkit-flex;
        display: -ms-flexbox;
        -ms-flex-wrap: wrap;
        margin: 0 auto;

        padding: 0;
        /* margin-inline-end: 174.85px; */
    }

    li {
        list-style: none;
        padding: 0 50px;

    }
</style>