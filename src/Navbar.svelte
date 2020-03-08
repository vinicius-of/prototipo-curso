<main>
    <nav>
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
    </nav>
</main>

<style>
    nav {
        background-color: aliceblue;
        display: flex;
        justify-content: space-around;
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
        font-size: 20px;
        margin: 0 12px;
    }

    a, a:focus, a:hover {
        color: black;
        text-decoration: none;
    }

    #btn-matricula {
        background-color: rgb(255, 102, 102);
        border-radius: 5px;
        padding: 10px;
        color: white;
    }
    
</style>