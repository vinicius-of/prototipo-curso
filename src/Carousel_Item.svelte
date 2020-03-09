<script>
    export let selected
</script>

<main>
    <div class={selected === true ? 'item selected':'item'}></div>
</main>

<style>

    .item {
        background-color: white;
        width: 325px;
        height: 500px;
        box-shadow: 0 0 30px rgba(0, 0, 0, 0.308);
        
    }

    .selected {
        z-index: 10;
        border-block-start: 8px solid #e84b60;
    }

</style>
