<template>
    <div class="header" :class="{fundo: background}">
            <a class="navbar-brand" @click="selectItem" href="#home">Vicente Crespo</a>
            <div class="header-items" :class="{fundo: background}">
                <a class="nav-item" @click="selectItem" :class="{selectedHeader: selected && selectedItem === 'desenvolvedor-header'}" id="desenvolvedor-header" href="#desenvolvedor">Sobre</a>
            
                <a class="nav-item" @click="selectItem" id="home-header" :class="{selectedHeader: selected && selectedItem === 'home-header'}" href="#cursos">Cursos</a>
            
                <a class="nav-item" @click="selectItem" :class="{selectedHeader: selected && selectedItem === 'projetos-header'}" id="projetos-header" href="#projetos">Projetos</a>
            
                <a class="nav-item" @click="selectItem" :class="{selectedHeader: selected && selectedItem === 'habilidades-header'}" id="habilidades-header" href="#habilidades">Habilidades</a>
            
                <a class="nav-item" @click="selectItem" :class="{selectedHeader: selected && selectedItem === 'contato-header'}" id="contato-header" href="#contato" >Contato</a>
            </div>             
    </div>
</template>

<script>
export default {
    name: 'header',
    data: function() {
        return {
            selected: false,
            selectedItem: '',
            background: false
        }
    },
    mounted() {
        window.addEventListener('wheel', this.handleScroll)
        window.addEventListener('scroll', this.detectScroll)
    },
    methods: {
        selectItem(e) {
            this.selectedItem = e.target.id
            this.selected = true
        },
        handleScroll(e) {
            this.selected = false
        },
        detectScroll(e) {
            if (window.scrollY >= window.screen.height) {
                this.background = true
            } else {
                this.background = false
            }
        }
    }
}
</script>

<style>
    .header {
        background: transparent;
        position: fixed;
        top: 0px;
        width: 100vw;
        height: 90px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        flex-wrap: wrap;
        padding: 10px 10px 0 10px;
        z-index: 2;
    }

    .fundo {
        background: rgb(21, 21, 21);
        border-bottom: 1px solid white;
    }

    .header-items {
        display: flex;
        justify-content: space-evenly;
        height: 100%;
        flex-wrap: wrap;
        width: 75%;
    }


    .header a {
        text-decoration: none;
        color: #fff;
    }

    .navbar-brand {
        border-bottom: 1px solid white;
        padding: 10px 20px 0px 20px;
        font-family: 'Dancing Script';
        font-size: 2.8rem;
        font-weight: bold;
        align-self: flex-start;
        justify-content: center;
        align-items: center;
        display: flex;
        width: 25%;
        height: 100%;
        margin: 0;
    }

    .nav-item {
        width: 20%;
        border-radius: 10px;
        padding: 10px;
        display: flex;
        height: calc(100% - 2px);
        align-items: center;
        justify-content: center;
    }

    .selectedHeader {
        border: 2px solid rgb(0, 110, 255);
        font-weight: bold;
    }

    .nav-item:hover {
        border: 2px solid rgb(0, 110, 255);
        font-weight: bold;
    }

    .navbar-brand:hover {
        color: rgb(0, 110, 255);
    }

    @media (max-width: 1010px) {
        .navbar-brand {
            width: 100%;
        }

        .header-items {
            width: 100%;
            height: 50%;
        }

        .nav-item {
            width: 20%;
            text-align: center;
        }

        .header {
            padding: 0;
        }
    }

    @media (max-width: 520px) {
        .header-items {
            height: 100%;
        }

        .nav-item {
            height: 50%;
        }

         .nav-item:nth-child(-n + 3) {
            width: 33%;
        }

        .nav-item:nth-child(n + 4) {
            width: 50%;
        } 
    }

    @media (max-width: 250px) {
        .header-items {
            display: none;
        }
    }


</style>