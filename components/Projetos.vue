<template>
    <div id="projetos" class="main-content">
        <h1>Projetos</h1>
        <div class="card-projetos">
            <div class="projeto">
                <b-card>
                    <b-card-img src="../static/qrcode-site.png" alt="Image" class="mb-2"></b-card-img>
                    <b-card-title>Gerador QR Code</b-card-title>
                    <b-card-text>
                        Aplicação Web em que você consegue gerar um QR Code para qualquer URL que digitar.
                    </b-card-text>
                    <b-button href="https://gerador-qrc-ode.vercel.app/" target="_blank" variant="primary">Testar Aplicação</b-button>
                    <b-button href="https://github.com/vicentecrespop/Gerador-QRCode" target="_blank" variant="secondary">Ver Projeto</b-button>
                </b-card>
            </div>
            <div class="projeto">
                <b-card>
                    <b-card-img src="../static/site-gastosmensais.png" alt="Image" class="mb-2"></b-card-img>
                    <b-card-title>Gastos Mensais</b-card-title>
                    <b-card-text>
                        Aplicação Web em que você cadastra os seus gastos mensais.
                    </b-card-text>
                    <b-button href="https://vue-gastos-mensais.vercel.app/" target="_blank" variant="primary">Testar Aplicação</b-button>
                    <b-button href="https://github.com/vicentecrespop/VueGastosMensais" target="_blank" variant="secondary">Ver Projeto</b-button>
                </b-card>
            </div>
            <div class="projeto">
                <b-card>
                    <b-card-img src="../static/calculadora-site.png" alt="Image" class="mb-2"></b-card-img>
                    <b-card-title>Calculadora de Celular</b-card-title>
                    <b-card-text>
                        Aplicação Web que simula a calculadora de um celular.
                    </b-card-text>
                    <b-button href="https://calculadora-celular.vercel.app/" target="_blank" variant="primary">Testar Aplicação</b-button>
                    <b-button href="https://github.com/vicentecrespop/CalculadoraCelular" target="_blank" variant="secondary">Ver Projeto</b-button>      
                </b-card>
            </div>
            <div class="projeto">
                <b-card>
                    <b-card-img src="../static/alwaysbmx-site.png" alt="Image" class="mb-2"></b-card-img>
                    <b-card-title>Always BMX</b-card-title>
                    <b-card-text>
                        Loja Virtual de peças e roupas de bicicletas BMX.
                    </b-card-text>
                    <b-button href="https://e-commerce-stripe-teste.vercel.app/" target="_blank" variant="primary">Testar Aplicação</b-button>
                    <b-button href="https://github.com/vicentecrespop/e-commerce-stripe" target="_blank" variant="secondary">Ver Projeto</b-button>      
                </b-card>
            </div>
            <div class="projeto">
                <b-card>
                    <b-card-img src="../static/Site-McDonalds.jpg" alt="Image" class="mb-2"></b-card-img>
                    <b-card-title>Cópia Site McDonalds Brasil</b-card-title>
                    <b-card-text>
                        Aplicação frontend do template do site do McDonalds Brasil.
                    </b-card-text>
                    <b-button href="https://mc-donalds-template.vercel.app/" target="_blank" variant="primary">Testar Aplicação</b-button>
                    <b-button href="https://github.com/vicentecrespop/McDonaldsTemplate" target="_blank" variant="secondary">Ver Projeto</b-button>      
                </b-card>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProjetosComponent'
}
</script>

<style>
    #projetos {
        display: flex;
        flex-direction: column;
        height: auto;
        min-height: 100vh;
    }

    .card {
        max-width: 20rem;
        height: 450px;
        background: transparent;
    }

    .card-img {
        height: 240px;
    }

    .card-projetos {
        margin-top: 10px;
        height: 100%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-evenly;
        align-items: center;
    }

    .projeto {
        margin: 20px;
        border: 1px solid #fff;
        border-radius: 10px;
    }

    .projeto:hover {
        border: 3px solid rgb(0, 110, 255);
        border-radius: 10px;
    }

    .titulo-projetos {
        background-color: #081C15;
        color: #fff;
    }

    @media (max-width: 1460px) {
        .projeto {
            margin: 50px 90px 40px 90px;
        }
    }

    @media (max-width: 1030px) {
        .card-projetos {
            flex-direction: column;
        }

        #projetos {
            height: auto;
        }
    }

    @media (max-width: 340px) {
        .card {
            height: 300px;
            max-width: 10rem;
        }

        .card-img {
            height: 120px;
        }

        .card-text {
            display: none;
        }

        .card-title {
            font-size: 0.8rem;
        }

        .projeto .btn {
            font-size: 0.8rem;
            width: 100%;
            margin-top: 5px;
        }
    }

    @media (max-width: 175px) {
        .projeto .btn {
            font-size: 0.4rem;
        }
    }
</style>



