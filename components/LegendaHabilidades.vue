<template>
    <div class="legendaHabilidades w-100 d-flex">
        <span>Nível de Conhecimento / Habilidade</span>
        <div class="barraHabilidade d-flex">
            <b-progress class="w-100" :max="100" height="3.5rem">
                <b-progress-bar :value="carregar" animated>
                    <span>{{ nomeHabilidade }}</span>
                </b-progress-bar>
            </b-progress>
            <span id="nivel">{{ habilidade }}%</span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'LegendaHabilidades',
    data: function() {
        return {
            carregar: 0
        }
    },
    props: {
        nomeHabilidade: {
            type: String,
            required: true
        },
        habilidade: {
            type: String,
            required: true
        }
    },
    mounted() {
        const carregarBarra = window.setInterval(() => {
            this.carregar += this.carregar < this.habilidade ? this.habilidade / 10 : 0
        }, 1)
        
        window.setTimeout(() => {
            clearInterval(carregarBarra)
        }, 110)
    }
}
</script>

<style>
    .legendaHabilidades {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        font-family: 'Courier New', Courier, monospace;
        animation:forwards 2s;
        font-size: 2rem;
    }

    .legendaHabilidades span:first-child {
        font-size: 1.5rem;
        padding: 15px;
    }

    .barraHabilidade {
        width: 480px;
    }

    .barraHabilidade span#nivel {
        border: 2px solid white;
        margin-left: 5px;
        padding: 2px;
        border-radius: 5px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .progress-bar {
        font-size: 1.5rem;
        transition-property: width;
        transition-duration: 2s;
    }

    .progress {
        padding: 1px;
    }

    @media (max-width: 560px) {
        .legendaHabilidades span:first-child {
            font-size: 1rem;
        }

        .barraHabilidade {
            width: 350px;
        }
    }
    
    @media (max-width: 370px) {
        .legendaHabilidades span:first-child {
            text-align: center;
        }

        .barraHabilidade {
            width: 250px;
        }
    }
</style>