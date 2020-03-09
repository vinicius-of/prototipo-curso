<main>
    <nav>
        <div>
            <ul>
                <li><div id="logo">Logo</div></li>
                <li><a href="#">Como funciona</a></li>
                <li><a href="#">Planos</a></li>
                <li><a href="#">Contato</a></li>
            </ul>
            <ul>
                <li><a href="#">Entrar</a></li>
                <li><a href="#" id="btn-matricula">Matricular-se</a></li>
            </ul>
        </div>
    </nav>
</main>

<style>

    * {
        font-size: 20px;
        padding: 0;
    }
    nav {
        background-color: aliceblue;
    }

    nav > div {
        max-width: 1200px;
        display: flex;
        justify-content: space-between;
        width: 90%;
        margin: 0 auto;
    }

    ul {
        display: flex;
        justify-content: space-around;
        align-items: center;
    }

    li {
        list-style: none;
        margin: 0 8px;
    }

    #logo {
        font-size: 30px;
        margin-right: 15px;
    }

    a, a:focus, a:hover {
        color: black;
        text-decoration: none;
    }

    #btn-matricula {
        background-color: #e84a61;
        border-radius: 5px;
        padding: 10px;
        color: white;
    }
    
</style>