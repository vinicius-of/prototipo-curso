<main>
    <div class="showup">
        <div class="title-content">
            <h1>Cursinhos da Ordem dos Advogados do Brasil e diversas outras áreas</h1>
            <p>Venha para o local que mais aprova candidatos no Brasil!</p>
            <a href="estudar">Comece a estudar agora</a>
        </div>
        <div class="image-content">
            <img src="./assets/apresentacao.png" alt="Imagem de aprensentação">
        </div>
    </div>
    
    <h3>Mais procurados</h3>
    <ul class="content-boxes">
        <li><div></div></li>
        <li><div></div></li>
        <li><div></div></li>
        <li><div></div></li>
        <li><div></div></li>
        <li><div></div></li>
    </ul>
</main>

<style>
    main {
        /* padding-left: 208px; */
        max-width: 1522px;
        margin: 0 208px;
    }

    a:hover {
        text-decoration: none;
    }

    li {
        list-style: none;
    }

    img {
        position: absolute;
        width: 1364.5px;
        height: 798.5px;
        left: 30%;
        top: 0px;
        z-index: -1;
        overflow-x: hidden;
    }

    .showup {
        display: block;
        margin-bottom: 380px;
    }

    .title-content > h1{
        font-weight: 500;
        font-size: 48px;
        line-height: 58px;
        max-width: 965px;
    }

    .title-content > p {
        font-size: 30px;  
        color: #A6A6A6;
        margin-bottom: 34px;
    }

    .title-content > a {
        background-color: #e84a61;
        border: none;
        border-radius: 5px;
        color: white;
        font-size: 28px;
        padding: 17px 75px;
        white-space: nowrap;
    }

    h3 {
        font-style: normal;
        font-weight: 900;
        font-size: 36px;
        line-height: 43px;
        color: #E84A5F; 
    }

    .content-boxes {
        padding: 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;

        display: -ms-flexbox;
        display: -webkit-flex;
        -ms-flex-wrap: wrap;
    }

    .content-boxes > li {
        background-color: #C4C4C4;
        width: 477px;
        height: 224px;
        text-align: center;
        margin-block-end: 27px;
    }
</style>