<script>
    import Navbar from './Navbar.svelte'
    import Content from './Content.svelte'
    import Team from './Team.svelte'
    import Prices from './Prices.svelte'
</script>

<main>
    <div>
        <Navbar />
        <Content />
        <Team />
        <Prices />
    </div>
</main>

<style>
    /* Background image*/

    div {
        background: url('../assets/apresentacao.png') no-repeat right top;
        background-size: 80%;
    }

	@media only screen and (max-width: 1764px) {
        div {
            background-position-x: 105%;
            background-position-y: 100px;
        }
    }

    @media only screen and (max-width: 1500px) {
        div {
            background-position-y: 250px;
        }
    }

    @media only screen and (max-width: 1195px) {
        div {
            background: none;
        }
    }

</style>