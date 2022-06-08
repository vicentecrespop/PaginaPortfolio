<template>
    <div id="cursos" class="main-content">
        <h1>Cursos / Certificados</h1>
        <div class="curso">
            <div class="duracao">
                <h2>IFSC</h2>
                <p>Agosto 2018 - Atualmente</p>
            </div>
            <a href="https://www.ifsc.edu.br/curso-aberto/-/asset_publisher/nvqSsFwoxoh1/content/id/1035537?p_r_p_564233524_categoryId=656799" target="_blank">
                <img src="https://media-exp1.licdn.com/dms/image/C560BAQHaOtOGVic9IA/company-logo_100_100/0/1519903450223?e=1662595200&v=beta&t=re9nvJ2Z-PcEabyW73-xs8yxeQ8ElVp00gyHo4p6VYE" alt="IFSC">
            </a>
            <div class="aprendizado">
                <h3>Curso de Graduação de Engenharia Eletrônica</h3>
                <ul>
                    <li>Linguagens de Programação (C)</li>
                </ul>
            </div>
        </div>
        <div class="curso">
            <div class="duracao">
                <h2>Cod3r Cursos</h2>
                <p>Janeiro 2022 - Maio 2022</p>
            </div>
            <a title="Clique para ver Certificado" href="https://www.udemy.com/certificate/UC-dc0134a1-afcb-4315-92fd-58818e269681/" target="_blank">
                <img src="https://media-exp1.licdn.com/dms/image/C560BAQEqmVRp2Q2Jbg/company-logo_100_100/0/1554852395434?e=1662595200&v=beta&t=QeUNvxvbgcosyAWnMeVlAKcFrg7fUwHH9BJ7SIur1d8" alt="Cod3r">
            </a>
            <div class="aprendizado">
                <h3>
                Curso Web Moderno Completo com JavaScript 2022 + Projetos    
                </h3>
                <ul>
                    <li>Linguagens Web (JavaScript, HTML5, CSS, TypeScript)</li>
                    <li>Frameworks (JQuery, Angular 9, VueJS, React, Express, Bootstrap)</li>
                    <li>Banco de Dados (MySQL, NoSQL, MongoDB, PostgreSQL)</li>
                    <li>Tecnologias (NodeJS, Gulp, Webpack, Sass)</li>
                </ul>
            </div>
        </div>
        <div class="curso">
            <div class="duracao">
                <h2>Harvard</h2>
                <p>Novembro 2021 - Março 2022</p>
            </div>
            <a title="Clique para ver Certificado" href="https://certificates.cs50.io/a21597d9-a698-4233-9eb7-e6a6c38f599c.pdf?size=letter" target="_blank">
                <img src="https://media-exp1.licdn.com/dms/image/C4E0BAQGYjmmBCvqLmg/company-logo_100_100/0/1519878692497?e=1662595200&v=beta&t=9-Tl742P4gEjQ32RDLEJGGHBa_Wwalu8t9ZSySUM-Cc" alt="CS50x">
            </a>
            <div class="aprendizado">
                <h3>Curso CS50x de Ciências da Computação</h3>
                <ul>
                    <li>Linguagens de Programação (C, Python, JavasScript)</li>
                    <li>Frameworks (Flask, Bootstrap)</li>
                    <li>Banco de Dados (SQLite3)</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'CursosComponent'
}
</script>

<style>
    #cursos {
        flex-direction: column;
        align-items: center;
        font-family: 'Courier New', Courier, monospace;
    }

    #cursos h1 {
        margin-bottom: 80px;
    }

    .duracao {
        width: 25%;
        padding-right: 30px;
        text-align: right;
    }

    .duracao h2 {
        color: rgb(0, 110, 255);
    }

    .curso {
        display: flex;
        justify-content: flex-end;
        width: 75%;
        margin-top: 20px;
    }

    .curso a {
        padding: 5px;
        height: 120px;
        width: 120px;
        border: 2px solid white;
    }

    .curso a:hover {
        border: 2px solid rgb(0, 110, 255);
    }

    .curso a img {
        height: 100%;
        width: 100%;
    }

    .curso .aprendizado {
        margin-left: 30px;
        width: 50%;
    }

    .aprendizado h3 {
        font-size: 1.5rem;
        text-align: justify;
        border-bottom: 2px solid rgb(0, 110, 255);
    }

    @media (max-width: 1430px) {
        #cursos {
            height: auto;
        }
    }

    @media (max-width: 810px) {
        .curso {
            flex-direction: column;
            align-items: center;
            width: 100%;
        }

        .curso .aprendizado {
            width: 75%;
            margin-top: 30px;
            margin-left: 0;
        }

        .curso .duracao {
            width: 100%;
            text-align: center;
            padding-right: 0;
        }
    }
</style>