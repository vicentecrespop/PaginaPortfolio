<template>
    <div class="footer-comp">
        <span>Site criado por Vicente Crespo.</span>
    </div>
</template>

<script>
export default {
    name: 'FooterComponent'
}
</script>

<style>
    .footer-comp {
        height: auto;
        width: 100%;
        padding-top: 20px;
        font-family: 'Courier New', Courier, monospace;
        background-color: rgb(21, 21, 21);
        color: #fff;
        z-index: 1;
        text-align: center;
    }

    @media (max-width: 344px) {
        .footer-comp {
            font-size: 0.8rem;
            height: auto;
        }
    }
</style>