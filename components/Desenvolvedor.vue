<template>
    <div id="desenvolvedor" class="main-content">
        <div class="perfil-foto d-flex flex-column">
            <div class="foto">
                <img src="../static/perfil-lg.jpg" alt="Foto">
            </div>
            <a href="#contato">Contato</a>
            <a href="/VicenteCrespo-CV.pdf" target="_blank">Baixar CV</a>
           <div class="loc">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-pin-map" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M3.1 11.2a.5.5 0 0 1 .4-.2H6a.5.5 0 0 1 0 1H3.75L1.5 15h13l-2.25-3H10a.5.5 0 0 1 0-1h2.5a.5.5 0 0 1 .4.2l3 4a.5.5 0 0 1-.4.8H.5a.5.5 0 0 1-.4-.8l3-4z"/>
                    <path fill-rule="evenodd" d="M8 1a3 3 0 1 0 0 6 3 3 0 0 0 0-6zM4 4a4 4 0 1 1 4.5 3.969V13.5a.5.5 0 0 1-1 0V7.97A4 4 0 0 1 4 3.999z"/>
                </svg>
                <span>Florianópolis - SC</span>
            </div>
        </div>
        <div class="dev">
            <div class="apresentacao">
                <h1>Desenvolvedor Web / Full Stack</h1>
                <div class="texto">
                    <p>
                        Estudante de Engenharia Eletrônica no Instituto Federal de Santa Catarina. 
                        Descobri programação na faculdade, estudando a linguagem C, procurei aprender
                        mais sobre programação e desenvolvimento de software através de videos e cursos online.
                    </p>
                    <p>
                        Completei os cursos CS50x de ciências da computação de Harvard, cujo foco principal é o desenvolvimento Back End em linguagens como C e Python,
                        e o curso Web Moderno de JavaScript da Cod3r, onde o foco é desenvolvimento Web / Front End mas também ensina tecnologias para o Back End.
                    </p>
                    <p>    
                        Sou um desenvolvedor Full Stack, pois assim como consigo desenvolver aplicações web voltadas ao Front End e com design responsivo,
                        consigo também trabalhar com banco de dados e a parte do Back End de aplicações. 
                    </p>
                </div>
            </div>
            <div class="redes-sociais d-flex justify-content-center">
                <a href="https://github.com/vicentecrespop" target="_blank">
                    <img src="../static/github-logo.png" alt="Github">
                </a>
                <a href="https://www.linkedin.com/in/vicente-crespo-733251238/" target="_blank">
                    <img src="../static/linkedin-perfil.png" alt="Linkedin">
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'DesenvolvedorComponent'
}
</script>

<style>
    #desenvolvedor {
        padding-top: 200px;
        font-family: 'Courier New', Courier, monospace;
        height: auto;
        min-height: 100vh;
    }

    .texto {
        width: 70%;
        border: 1px solid #fff;
        box-shadow: 10px 10px 10px #000;
        padding: 20px;
        text-align: justify;
        margin-top: 30px;
    }

    .foto {
        border: 2px solid rgb(0, 110, 255);
        border-radius: 500px;
        width: 220px;
        height: 220px;
        overflow: hidden;
    }

    .perfil-foto {
        align-items: flex-end;
        width: 30%;
        margin: 30px;
    }

    .perfil-foto a {
        border: 2px solid #fff;
        width: 220px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 10px;
        text-decoration: none;
        margin-top: 5px;
        color: #fff;
    }

    .loc {
        width: 220px;
        text-align: center;
        padding: 10px;
    }

    .perfil-foto a:hover {
        border: 2px solid rgb(0, 110, 255);
        color: #ccc;
    }

    .foto img {
        width: 320px;
        height: 380px;
        margin: -45px 0 0 -40px;
    }

    .dev {
        display: flex;
        flex-direction: column;
        height: 100%;
        width: 70%;
    }

    .apresentacao {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .redes-sociais {
        height: 200px;
        align-items: center;
    }

    .redes-sociais a {
        margin-left: 20px;
    }

    .redes-sociais img {
        width: 70px;
        height: 70px;
    }

    @media (max-width: 1460px) {
        #desenvolvedor {
            height: auto;
        }
    }

    @media (max-width: 730px) {
        #desenvolvedor {
            flex-direction: column;
            align-items: center;
        }

        .perfil-foto {
            width: 100%;
            align-items: center;
        }

        .dev {
            width: 100%;
            justify-content: center;
        }
    }

    @media (max-width: 570px) {
        #desenvolvedor {
            height: auto;
        }
    }

</style>