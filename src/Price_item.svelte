<script>
    export let selected

    let container
</script>

<div>
    <div class={selected === true ? 'item selected' : 'item'}></div>
</div>

<style>

    .item {
        background-color: white;
        width: 350px;
        height: 640px;
        box-shadow: 0px 4px 74px rgba(0, 0, 0, 0.25);
    }

    .selected {
        position: absolute;
        width: 450px;
        height: 700px;
        left: 50%;
        top: 50%;
        transform: translate(-50%,-50%);
        border-block-start: 8px solid #E84A5F;
    }

    @media only screen and (max-width: 745px) {
        .item {
            width: 345px;
            margin: 15px;
        }

        .selected {
            left: 0;
            top: 0;
            transform: translate(0, 0);
            display: block;
            position: relative;
            border-block-start: none;
            width: 350px;
            height: 640px;
        }
    }

</style>
