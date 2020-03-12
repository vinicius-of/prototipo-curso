<script>
    import Prices from './Price_item.svelte';

    const itemList = [
        false,
        true,
        false
    ]

</script>

<section>
    <p>Sabe quando você pode começar? <strong>Agora!</strong></p>
    <ul class="carousel">
        {#each itemList as item}
            <li><Prices selected={item} /></li>
        {/each}
    </ul>
</section>

<style>
    li {
        list-style: none;
    }

    p {
        font-style: normal;
        font-size: 40px;
        line-height: 86px;
        text-align: center;
        margin: 65px 50px; 
    }

    .carousel {
        padding: 0 15%;
        margin-bottom: 100px; 

        position: relative;
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    @media only screen and (max-width: 745px) {
        .carousel {
            flex-wrap: wrap;
        }
    }

</style>