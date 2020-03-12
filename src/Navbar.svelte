
<script>
    import {fly} from 'svelte/transition';
    let menuDropped = false;

    function handleClickMenu() {
        if(!menuDropped) menuDropped = true
        else menuDropped = false
    }

</script>

<nav>
    <div class="container">
        <ul class="navbar">
            <h1 class="logo">Logo</h1>
            <li><a href="#">Como funciona</a></li>
            <li><a href="#">Planos</a></li>
            <li><a href="#">Contato</a></li>
        </ul>
        <ul class="navbar">
            <li><a href="#">Entrar</a></li>
            <li><button id="btn-matricula">Matricule-se</button></li>
        </ul>

        <div class="responsive-navbar">
            <h1 class="logo">Logo</h1>
            <button
            on:click={handleClickMenu}
            id="btn-menu"><i class="material-icons">menu</i></button>

            {#if menuDropped}
                <div 
                transition:fly={{y: -400, duration: 200}}
                class="menu-dropdown">

                    <ul>
                        <li><a href="#">Entrar</a></li>
                        <li><a href="#">Matricule-se</a></li>
                        <li><a href="#">Como funciona</a></li>
                        <li><a href="#">Planos</a></li>
                        <li><a href="#">Contato</a></li>
                    </ul>
                </div>
            {/if}
        </div>
    </div>
</nav>

<style>

    * {
        font-size: 25px;
        padding: 0;
    }

    a, a:focus, a:hover {
        color: black;
        text-decoration: none;
    }
    
    li {
        list-style: none;
        margin: 0 31.5px;
    }

    .container {
        display: flex;
        align-self: center;
        justify-content: space-between;

        margin: 0 auto;
        max-width: 79%;
    }

    .container .navbar {
        display: flex;
        align-items: center;

        margin-block-start: 0;
        margin-block-end: 0;
    }

    #btn-matricula {
        background-color: #e84a61;
        border-radius: 5px;
        color: white;
        padding: 12px;
        cursor: pointer;
    }

    .logo {
        margin: 0;
        padding: 0;
        font-style: normal;
        font-weight: normal;
        font-size: 64px;
        line-height: 75px;

        margin-inline-end: 94px;
    }

    .responsive-navbar {
        display: none;
        position: relative;
        border-block-end: 2px solid black;
        width: 100%;
    }

    .menu-dropdown {
        position: absolute;
        top: 102%;
        left: 0;
        width: 100%;
        background-color: #e84a61;
    }

    .menu-dropdown ul {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-block-start: 0;
        margin-block-end: 0;
    }

    .menu-dropdown li {
        width: 100%;
        height: 50px;
        border-block-end: 1.5px solid black;
        text-align: center;
    }

    .menu-dropdown a {
        color: white;
    }

    #btn-menu {
        margin: 0;
        color: white;
        background-color: #e84a61;
        border: none;
        outline: none;
        padding: 10px;
        border-radius: 10%;
        margin-right: 10px;
    }

    #btn-menu i {
        font-size: 45px;
    }

    /* Diminuindo o tamanho da logo e diminuindo a margem do elementos li */
    
    @media only screen and ( max-width: 1419px) {

        .container .navbar {
            justify-content: flex-start;
        }

        li {
            margin: 0 20px;
        }

        .logo {
            margin-right: 30px;
            font-size: 50px;
        }
    }

    /* Retirando o navbar normal para ser substituido pelo responsive-navbar */

    @media only screen and (max-width: 950px) {
        .container {
            max-width: 100%;
            justify-content: center;
            background-color: #e84a61;
        }
        .navbar {
            display: none !important;
        }

        .responsive-navbar{
            display: flex;
            justify-content: space-between;
            align-items: center;
            
        }

        .logo {
            font-size: 30px;
            margin-left: 25px; 
            color: white;
        }

    }
</style>