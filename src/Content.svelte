<script>
    import {Link, Route, Router} from 'svelte-routing';
    import Video from './Videoplayer.svelte';

    let url = "";
</script>

<section>
    <div class="showup">
        <div class="title-content">
            <h1>Cursinhos da Ordem dos Advogados do Brasil e diversas outras áreas</h1>
            <p>Venha para o local que mais aprova candidatos no Brasil!</p>
            <button>Comece a estudar agora</button>
        </div>
    </div>
    
    <h3 class="title">Mais procurados</h3>
    <ul class="content-boxes">
        <li><div></div></li>
        <li><div></div></li>
        <li><div></div></li>
        <li><div></div></li>
        <li><div></div></li>
        <li><div></div></li>
    </ul>
</section>

<style>
    section {
        max-width: 80%;
        margin: 0 auto;
    }

    a:hover {
        text-decoration: none;
    }

    li {
        list-style: none;
    }

     .title {
        font-style: normal;
        font-weight: 900;
        font-size: 36px;
        line-height: 43px;
        color: #E84A5F; 
    }

    .title-content {
        margin-bottom: 380px;
    }


    .title-content > h1{
        font-weight: 500;
        font-size: 48px;
        line-height: 58px;
        max-width: 965px;

        margin-top: 125px;
    }

    .title-content > p {
        font-size: 30px;  
        color: #A6A6A6;
        margin-bottom: 34px;
    }

    .title-content > button {
        background-color: #e84a61;
        border: none;
        border-radius: 5px;
        color: white;
        font-size: 28px;
        padding: 17px 75px;
        cursor: pointer;
    }

    /* .title {
        width: 100%;
        text-align: center;
    } */

    .content-boxes {
        padding: 0;
        display: flex;
        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;

        display: -ms-flexbox;
        display: -webkit-flex;
        -ms-flex-wrap: wrap;
    }

    .content-boxes > li {
        background-color: #C4C4C4;
        max-width: 477px;
        width: 100%;
        height: 224px;
        text-align: center;
        margin: 14px;
    }

    @media only screen and (max-width: 1279px) {
        .title {
            text-align: center;
        }

        .content-boxes {
            justify-content: center;
        }
    }

</style>