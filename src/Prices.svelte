<script>
    import Prices from './Price_item.svelte';

    const itemList = [
        false,
        true,
        false
    ]

</script>

            <!-- {#each itemList as item}
                <li><Prices selected={item} /></li>
            {/each} -->

<main>
    <p>Sabe quando você pode começar? <strong>Agora!</strong></p>
    <ul class="carousel">
        <li><Prices /></li>
        <li><Prices selected={true} /></li>
        <li><Prices /></li>
    </ul>
</main>

<style>
    li {
        list-style: none;
    }

    p {
        font-style: normal;
        font-size: 72px;
        line-height: 86px;
        text-align: center;
        margin: 113px 0; 
    }

    .carousel {
        padding: 0;

        position: relative;
        display: flex;
        justify-content: space-around;
        align-items: center;

        /* display: flex;
        justify-content: space-around;
        align-items: center;

        display: -ms-flexbox;
        display: -webkit-flex; */
    }

</style>