<main>
    <nav>
        <div>
            <h1 id="logo">Logo</h1>
            <ul>
                <li><a href="#">Como funciona</a></li>
                <li><a href="#">Planos</a></li>
                <li><a href="#">Contato</a></li>
            </ul>
            <ul id="matricula">
                <li><a href="#">Entrar</a></li>
                <li><a href="#" id="btn-matricula">Matricular-se</a></li>
            </ul>
        </div>
    </nav>
</main>

<style>

    * {
        font-size: 28px;
        padding: 0;
        white-space: nowrap;
    }

    nav > div {
        padding-left: 208px;
        padding-right: 168px;
        
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 0 auto;
    }

    ul {
        display: flex;
        align-items: center;
    }

    li {
        list-style: none;
        margin-right: 63px;
    }

    #logo {
        margin: 0;
        padding: 0;
        font-style: normal;
        font-weight: normal;
        font-size: 64px;
        line-height: 75px;

        margin-right: 94px;
    }

    a, a:focus, a:hover {
        color: black;
        text-decoration: none;
    }

    #btn-matricula {
        background-color: #e84a61;
        border-radius: 5px;
        color: white;
        font-size: 28px;
        padding: 17px;
    } 
    
</style>