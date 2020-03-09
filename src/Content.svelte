<script></script>

<main>
    <div class="showup">
        <div class="title-content">
            <h1>Cursinhos da Ordem dos Advogados do Brasil e diversas outras áreas</h1>
            <p>Venha para o local que mais aprova candidadtos no Brasil!</p>
            <a href="#">Comece a estudar agora</a>
        </div>
        <div class="image-content">
            <img src="#" alt="Imagem: Pedir ao Matheus pela imagem">
        </div>
    </div>
    
    <h3>Mais procurados</h3>
    <ul class="content-boxes">
        <li><div>1</div></li>
        <li><div>2</div></li>
        <li><div>3</div></li>
        <li><div>4</div></li>
        <li><div>5</div></li>
        <li><div>6</div></li>
    </ul>
</main>

<style>
    main {
        width: 90%;
        max-width: 1200px;
        margin: 0 auto;
    }

    a:hover {
        text-decoration: none;
    }

    li {
        list-style: none;
        color: white;
    }

    .showup {
        display: flex;
        display: -webkit-flex;
        display: -ms-flexbox;
        margin-bottom: 200px;
    }

    .title-content > a {
        background-color: #e84a61;
        border: none;
        border-radius: 5px;
        color: white;
        font-size: 20px;
        padding: 10px 2.5rem;
    }

    .title-content > p {
        color: #b1b3b2;
    }

    h3 {
        color: red;   
    }

    .content-boxes {
        margin: 0;
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
        background-color: rgb(155, 155, 155);
        width: 30%;
        height: 150px;
        border: 1px solid black;
        text-align: center;
        margin-block-end: 10px;
    }
</style>