<script>
    export let selected
</script>

<main>
    <div class={selected === true ? 'item selected':'item'}></div>
</main>

<style>

    .item {
        background-color: white;
        width: 588px;
        height: 962px;
        box-shadow: 0px 4px 74px rgba(0, 0, 0, 0.25);
    }

    .selected {
        position: absolute;
        width: 643px;
        height: 1051px;
        left: 50%;
        top: 50%;
        transform: translate(-50%,-50%);
        border-block-start: 8px solid #E84A5F;
    }

</style>
