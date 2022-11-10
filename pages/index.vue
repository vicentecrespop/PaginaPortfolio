<template>
  <div class="app">    	
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script&display=swap" rel="stylesheet">   
    <img src="../static/fundo-home.jpg" alt="programador" id="imagem-inicial">
    <Header />
    <Home />
    <Desenvolvedor />
    <div class="espaco"></div>
    <Cursos />
    <div class="espaco"></div>
    <Projetos />
    <div class="espaco"></div>
    <HabilidadesSlider />
    <div class="espaco"></div>
    <Contato />
    <Footer />
  </div>
</template>

<script>
import Header from '../components/Header.vue'
import Home from '../components/Home.vue'
import Desenvolvedor from '../components/Desenvolvedor.vue'
import Projetos from '../components/Projetos.vue'
import Contato from '../components/Contato.vue'
import HabilidadesSlider from '../components/HabilidadesSlider.vue'
import Cursos from '../components/Cursos.vue'
import Footer from '../components/Footer.vue'
import { inject } from '@vercel/analytics'

export default {
  name: 'IndexPage',
  components: { Header, Cursos, Home, Desenvolvedor, Projetos, Contato, HabilidadesSlider, Footer },
  created() {
    inject()
  }
}
</script>

<style>
  html {
    scroll-behavior: smooth;
    background-color: rgb(21, 21, 21);
  }

  body {
    height: 100vh;
  }

  .app {
    display: flex;
    flex-direction: column;
  }

  .app #imagem-inicial {
    width: 100vw;
    height: 100vh;
    position: fixed;
    top: 0px;
    filter: brightness(30%);
    z-index: 0;
  }

  .main-content {
    padding-top: 120px;
    z-index: 1;
    height: 100vh;
    width: 100vw;
    background-color: rgb(21, 21, 21);
    display: flex;
    color: #fff;
  }

  .espaco {
    height: 30px;
  }

  @media (max-width: 1400px) {
    .app #imagem-inicial {
      width: 1400px;
      height: 1000px;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }

  @media (max-width: 1010px) {
    .main-content {
      padding-top: 200px;
    }


  }

  @media (max-width: 250px) {
    .main-content {
      padding-top: 120px;
    }
  }

</style>
