<script>
    import Profile from './Profile.svelte'
</script>

<section>
    <h1 class="title">Time</h1>
    <ul class="team-list">
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
        <li><Profile name={'Barros'} title={'Professor Dr. Ufal'} image={"./assets/placeholder-perfil.jpg"} /></li>
    </ul>
</section>
<style>
    section {
        width: 100%;
        background-color: #e84b60;
        margin: 75px 0;
    }

    .title {
        color: white;
        text-align: center;

        font-weight: 900;
        font-size: 40px;
        line-height: 86px;

        margin: 0;
        padding: 30px 0;
    }

    
    li {
        list-style: none;
        padding: 0 50px;
    }

    .team-list {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        max-width: 1199px;

        display: -webkit-flex;
        display: -ms-flexbox;
        -ms-flex-wrap: wrap;
        margin: 0 auto;

        padding: 0;
    }
</style>