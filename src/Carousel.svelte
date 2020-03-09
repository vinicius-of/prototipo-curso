<script>
    import Item from './Carousel_Item.svelte';

    const itemList = [
        false,
        true,
        false
    ]

</script>

<main>
    <p>Sabe quando você pode começar? <strong>Agora!</strong></p>
    <ul class="carousel">
        {#each itemList as item}
             <li><Item selected={item} /></li>
        {/each}
    </ul>
</main>

<style>
    li {
        list-style: none;
    }

    p {
        font-size: 30px;
        display: block;
        text-align: center;
    }

    .carousel {
        padding: 0;

        display: flex;
        justify-content: center;
        align-items: center;

        display: -ms-flexbox;
        display: -webkit-flex;
    }

</style>