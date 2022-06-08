<template>
    <div id="desenvolvedor" class="main-content">
        <div class="perfil-foto d-flex flex-column">
            <div class="foto">
                <img src="../static/foto-perfil.jpg" alt="Foto">
            </div>
            <a href="#contato">Contato</a>
            <a href="https://www.linkedin.com/ambry/?x-li-ambry-ep=AQLtIdiuJrQ0TQAAAYE-OQy2w6r2Mw93rk9UAGmYdzIIrOvibmRRguovRzUIc4FCKwKRPi_YU02Ujhfm8rP4l-vOcs764T3ZwBryeCAWoUMrZ2m9D3jWJA7sl-TFbWE6fUa_X5gCYDJT9ojoP92EqRFcdsS5kR_V3BQ198tR41I4nOBDVe6qeWlfvmZyLCUES9y8X0W6qG7OgDMxcGQkWU_Hba0qqSJGkn0SoBNQwOzEeiqAgNMj2bD_anOlv3NgD0CT_vIhmAnWE_us6JOTQrCEnjiMnlV69tII1cE2nVVPnKUGCXL-0dSoPuxhYrHht2qMBpnISIe3aQzgIP5Fp3smcJ9E3VIYA0qU_6WanwpzGHJRso7P1ChUljvTmCWj39KkkgA_o6fq8UKTwim2V324N8s7KrhlpMtb9GLkLw-rouwIYJWYqmab6bkCGvxFgHnEXA-oXaD8VLENWnu5u5s98KDLqn2IxYnRIPi1JI_dGPNY9PI65MB2zD3djYX5je7_SA9JpN04vfw10TIrw92sswJre3fbWtP4glIRKrOleqnJDVNFdpJ8cTF1xxMXyLqdIA&x-ambry-um-filename=Profile.pdf" target="_blank">Baixar CV</a>
        </div>
        <div class="dev">
            <div class="apresentacao">
                <h1>Desenvolvedor Web / Full Stack</h1>
                <div class="texto">
                    <p>
                        Estudante de Engenharia Eletrônica no Instituto Federal de Santa Catarina. 
                        Descobri programação na faculdade, estudando a linguagem C, e então procurei aprender
                        mais sobre programação e desenvolvimento de software através de videos e cursos online.
                    </p>
                    <p>
                        Já completei o curso CS50x de Harvard, que tinha como foco principal o desenvolvimento Back End em linguagens como C e Python,
                        e o curso Web Moderno da Cod3r, que tem como foco o desenvolvimento Web / Front End mas também ensina tecnologias para o Back End.
                    </p>
                    <p>    
                        Me considero um desenvolvedor Full Stack pois assim como consigo desenvolver aplicações web voltadas ao Front End e com design responsivo,
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
        height: 100vh;
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

    .perfil-foto a:hover {
        border: 2px solid rgb(0, 110, 255);
        color: #ccc;
    }

    .foto img {
        width: 230px;
        height: 220px;
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