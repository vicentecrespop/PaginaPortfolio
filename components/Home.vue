<template>
    <div id="home" class="main-content">
        <h1>Portfólio</h1>
        <p>Vicente Crespo</p>
        <p>Desenvolvedor Web / Full Stack</p>
    </div>
</template>

<script>
export default {
    name: 'HomeComponent'
}
</script>

<style>
    #home {
        flex-direction: column;
        align-items: center;
        padding-top: 300px;
        z-index: unset;
        color: #fff;
        background-color: #000;
    }

    #home h1 {
        font-size: 1.5em;
        font-family: 'Courier New', Courier, monospace;
        margin: 0;
        display: flex;
        justify-content: center;
        align-items: flex-end;
        padding: 0;
    }

    #home p:first-of-type {
        font-size: 4em;
        font-family: 'Dancing Script';
        margin: 0;
        height: 70px;
        display: flex;
        align-items: center;
    }

    #home p:last-of-type {
        font-size: 1.2em;
        font-family: 'Courier New', Courier, monospace;
    }

    #home img {
        width: 100vw;
        height: 100vh;
        position: absolute;
        top: 0px;
        opacity: 30%;
    }

    @media (max-width: 370px) {
        #home {
            font-size: 0.6rem;
        }
    }

    @media (max-width: 220px) {
        #home {
            font-size: 0.3rem;
        }
    }
</style>