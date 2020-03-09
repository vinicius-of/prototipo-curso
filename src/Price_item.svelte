<script>
    export let selected
</script>

<main>
    <div class={selected === true ? 'item selected':'item'}></div>
</main>

<style>

    .item {
        background-color: white;
        width: 643px;
        height: 1051px;
        box-shadow: 0px 4px 74px rgba(0, 0, 0, 0.25);
        
    }

    .selected {
        z-index: 10;
        border-block-start: 8px solid #e84b60;
    }

</style>
