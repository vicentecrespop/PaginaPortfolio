<template>
    <div id="contato" class="main-content">  
        <h1>Contato</h1>
        <div class="contato-conteudo">
            <div class="info">
                <a href="mailto:vicentecrespo45@gmail.com" target="_blank">
                    <div class="dados">
                        <img src="../static/email-logo.png" alt="Logo-Email">
                        <span>E-MAIL</span>
                        <p>vicentecrespo45@gmail.com</p>
                    </div>
                </a>
                <a href="https://api.whatsapp.com/send?phone=5548998497668&text=Bom%20Dia,%20Vicente." target="_blank">
                    <div class="dados">
                        <img src="../static/zap-logo.png" alt="Logo-Whatsapp">
                        <span>TELEFONE / WHATSAPP</span>
                        <p>(48) 998497668</p>
                    </div>
                </a>
                <a href="https://www.linkedin.com/in/vicente-crespo-733251238/" target="_blank">
                    <div class="dados">
                        <img src="../static/linkedin-logo.png" alt="Logo-Linkedin">
                        <span>LINKEDIN</span>
                    </div>
                </a>
                <a href="https://github.com/vicentecrespop" target="_blank">
                    <div class="dados">
                        <img src="../static/github-logo.png" alt="Logo-Github">
                        <span>GITHUB</span>
                    </div>
                </a>
            </div>
            <div class="formulario">
                <form action="https://formsubmit.co/1819f8e0fb7d54e37398316a9b4bcde0" method="POST" target="_blank">
                    <div class="form-group">
                        <div class="form-row">
                            <input type="text" name="name" class="form-control" placeholder="Nome" required>                        
                        </div>
                    </div>
                    <div class="form-group">
                        <div class="form-row">
                            <input type="text" name="email" class="form-control" placeholder="E-mail" required>                        
                        </div>
                    </div>
                    <div class="form-group">
                        <textarea placeholder="Mensagem" class="form-control" name="message" rows="10" required></textarea>
                    </div>
                    <button type="submit" class="btn btn-lg btn-dark btn-block">Enviar</button>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ContatoComponent'
}
</script>

<style>
    #contato {
        flex-direction: row;
        flex-wrap: wrap;
        color: #fff;
        font-family: 'Courier New', Courier, monospace;
    }

    .contato-conteudo {
        display: flex;
        width: 100%;
    }

    #contato a {
        text-decoration: none;
        color: #fff;
        margin: 5px;
    }

    #contato a:hover {
        text-decoration: none;
        color: #fff;
    }

    .formulario {
        width: 50%;
        padding: 30px;
    }

    .info {
        display: flex;
        flex-direction: row;
        width: 50%;
        justify-content: space-evenly;
        align-items: flex-start;
        flex-wrap: wrap;
    }

    .info a {
        width: 40%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .dados {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 10px;
        height: 200px;
        width: 250px;
    }

    .info .dados:hover {
        border: 1px solid rgb(0, 110, 255);
    }

    .info .dados span {
        margin-top: 10px;
        text-align: center;
        font-weight: bold;
        color: rgb(0, 110, 255);
    }

    .dados img {
        width: 50px;
        height: 50px;
    }

    h1 {
        font-family: 'Dancing Script';
        width: 100%;
        text-align: center;
    }

    @media (max-width: 1040px) {
        #contato {
            height: auto;
        }
    }

    @media (max-width: 1010px) {
        .dados img {
            width: 50px;
            height: 50px;
        }

        .info a {
            width: 100%;
        }

        .info {
            justify-content: center;
            align-items: center;
        }

        #contato {
            height: auto;
        }
    }

    @media (max-width: 510px) {
        .dados p {
            display: none;
        }

        .dados {
            width: 150px;
            height: 150px;
        }

    }

    @media (max-width: 490px) {
        .info a {
            width: 100%;
        }
    }


</style>