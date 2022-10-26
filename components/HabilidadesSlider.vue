<template>
<div id="habilidades" class="main-content">
    <div class="habilidades-slider">
        <h1>Habilidades</h1>
        <div class="zona-slider">
            <div class="botoes">
                <svg @click="anterior" xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="currentColor" class="bi bi-arrow-left-short" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M12 8a.5.5 0 0 1-.5.5H5.707l2.147 2.146a.5.5 0 0 1-.708.708l-3-3a.5.5 0 0 1 0-.708l3-3a.5.5 0 1 1 .708.708L5.707 7.5H11.5a.5.5 0 0 1 .5.5z"/>
                </svg>
                <svg @click="proximo" xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="currentColor" class="bi bi-arrow-right-short" viewBox="0 0 16 16">
                    <path fill-rule="evenodd" d="M4 8a.5.5 0 0 1 .5-.5h5.793L8.146 5.354a.5.5 0 1 1 .708-.708l3 3a.5.5 0 0 1 0 .708l-3 3a.5.5 0 0 1-.708-.708L10.293 8.5H4.5A.5.5 0 0 1 4 8z"/>
                </svg>
            </div>
            <div class="slider">
                <div class="slide">
                    <img src="../static/javascript-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" alt="JavaScript" conhecimento="90">
                </div>
                <div class="slide">
                    <img src="../static/css-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="95" alt="CSS">
                 </div>
                <div class="slide">
                    <img src="../static/html-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="95" alt="HTML"> 
                </div>
                <div class="slide">
                    <img src="../static/python-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="85" alt="Python ">
                </div>
                <div class="slide">
                    <img src="../static/angularjs-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="76" alt="Angular">
                </div>
                <div class="slide">
                    <img src="../static/linux-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="80" alt="Linux" >
                </div>
                <div class="slide">
                    <img src="../static/bootstrap-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="85" alt="Bootstrap">
                </div>
                <div class="slide">
                    <img src="../static/c-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="90" alt="C">
                 </div>
                <div class="slide">
                    <img src="../static/flask-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="80" alt="Flask">
                </div>
                <div class="slide">
                    <img src="../static/jquery-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="90" alt="JQuery">
                </div>
                <div class="slide">
                    <img src="../static/mongodb-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="95" alt="MongoDB">
                </div>
                <div class="slide">
                    <img src="../static/mysql-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="90" alt="MySQL">
                </div>
                <div class="slide">
                    <img src="../static/nodejs-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="90" alt="NodeJS">
                </div>
                <div class="slide">
                    <img src="../static/nuxtjs-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="90" alt="NuxtJS">
                </div>
                <div class="slide">
                    <img src="../static/reactjs-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="85" alt="ReactJS">
                </div>
                <div class="slide">
                    <img src="../static/sql-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="90" alt="SQL">
                 </div>
                <div class="slide">
                    <img src="../static/vuejs-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="95" alt="VueJS">
                </div>
                <div class="slide">
                    <img src="../static/sass-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="80" alt="Sass">
                </div>
                <div class="slide">
                    <img src="../static/typescript-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="85" alt="TypeScript">
                </div>
                <div class="slide">
                    <img src="../static/postgresql-logo.png" @mouseleave="resetaNome" @mouseenter="mostraNome" conhecimento="80" alt="PostgreSQL">
                </div>
            </div>
        </div>
        <div class="legenda-espaco">
            <div class="detalhes" v-if="!mostrar">
                <span>Passe o mouse para ver mais</span>
            </div>
            <LegendaHabilidades class="fadeIn" v-if="mostrar" :nomeHabilidade="nomeHabilidade" :habilidade="habilidade"/>
        </div>
    </div>
</div>
</template>

<script>
import LegendaHabilidades from './LegendaHabilidades.vue'

export default {
    name: 'HabilidadesSlider',
    components: { LegendaHabilidades },
    data: function() {
        return {
           avancar: 0,
           nomeHabilidade: '',
           habilidade: '',
           mostrar: false,
           habilidadeAtual: 0,
           quantidadeHabilidades: 0,
           larguraHabilidade: 0,
           larguraSlider: 0
        }
    },
    methods: {
        proximo() {
            const slider = document.getElementsByClassName('slider')
            this.larguraSlider = slider[0].getBoundingClientRect().width
            const slides = document.querySelectorAll('div.slide')
            const limite = this.larguraSlider === 540 ? 8 : 4
            const pular = this.larguraSlider === 540 ? 4 : 2
            const avancarImagens = this.habilidadeAtual >= limite ? pular : this.habilidadeAtual - pular
            this.avancar += this.larguraHabilidade * avancarImagens
            this.habilidadeAtual -= avancarImagens
            slides.forEach(slide => slide.style.right = `${this.avancar}px`)
        },
        anterior() {
            const slider = document.getElementsByClassName('slider')
            this.larguraSlider = slider[0].getBoundingClientRect().width
            const slides = document.querySelectorAll('div.slide')
            const pular = this.larguraSlider === 540 ? 4 : 2
            const limite = this.quantidadeHabilidades - pular
            const avancarImagens = this.habilidadeAtual <= limite ? pular : this.quantidadeHabilidades - this.habilidadeAtual 
            this.avancar -= this.larguraHabilidade * avancarImagens
            this.habilidadeAtual += avancarImagens
            slides.forEach(slide => slide.style.right = `${this.avancar}px`)
        },
        mostraNome(e) {
            this.nomeHabilidade = e.target.alt
            this.habilidade = e.target.getAttribute('conhecimento')
            this.mostrar = true
        },
        resetaNome() {
            this.nomeHabilidade = ''
            this.habilidade = 0
            this.mostrar = false
        }
    },
    mounted() {
        const slides = document.querySelectorAll('div.slide')
        this.habilidadeAtual = slides.length
        this.quantidadeHabilidades = slides.length
        this.larguraHabilidade = slides[0].getBoundingClientRect().width + 10
    }
}
</script>

<style>
    @-webkit-keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 1; } 
    }
    @-moz-keyframes fadeIn {
    0% { opacity: 0;}
    100% { opacity: 1; }
    }
    @-o-keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 1; }
    }
    @keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 1; }
    }

    .fadeIn {
        -webkit-animation: fadeIn 1s ease-in-out;
        -moz-animation: fadeIn 1s ease-in-out;
        -o-animation: fadeIn 1s ease-in-out;
        animation: fadeIn 1s ease-in-out;
        z-index: 1;
    }

    #habilidades {
        display: flex;
        justify-content: center;
        height: auto;
        min-height: 100vh;
    }

    .detalhes {
        font-family: 'Courier New', Courier, monospace;
        margin-top: 5px;
    }

    .habilidades-slider {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .zona-slider {
        margin-top: 100px;
        z-index: 2;
    }

    .legenda-espaco {
        height: 8rem;
        margin-bottom: 30px;
    }

    .botoes {
        display: flex;
        justify-content: flex-end;
        padding-bottom: 10px;
    }

    .botoes svg {
        margin-left: 10px;
        border: 2px solid #fff;
        border-radius: 5px;
    }

    .botoes svg:hover {
        color: #aaa;
        border: 2px solid #aaa;
    }

    .botoes svg:active {
        border: 2px solid rgb(0, 110, 255);
        color: rgb(0, 110, 255);
    }

    .slider {
        border: 2px solid white;
        width: 540px;
        height: 140px;
        overflow: hidden;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        position: relative;
        align-items: center;
    }

    .habilidades-slider img {
        height: 100px;
        width: 100px;
    }

    .slide {
        position: relative;
        padding: 10px;
        right: 0px;
        transition-property: right;
        transition-duration: 1s;
        border: 2px solid white;
        margin: 5px;
    } 

    .slide:hover {
        border: 2px solid rgb(0, 110, 255);
    }

    .nomeHabilidade {
        font-family: 'Dancing Script';
        font-size: 3rem;
        padding-top: 30px;
    }

    @media (max-width: 560px) {
        .slider {
            width: 273px;
        }
    }

    @media (max-height: 600px) {
        #habilidades {
            height: auto;
        }
    }
</style>