<template>

    <div id="container">

        <!-- Parte sinistra -->
        <span class="button">
            <div>sign-up now!</div>
        </span>

        <!-- Parte destra -->
        <div class="block-right">
            <div><span>follow us</span></div>
            <div><img src="../../assets/loghi/footer-facebook.png" alt="Logo Facebook" style="width: 35px; height:35px">
            </div>
            <div><img src="../../assets/loghi/footer-twitter.png" alt="Logo Twitter" style="width: 35px; height:35px">
            </div>
            <div><img src="../../assets/loghi/footer-youtube.png" alt="Logo Youtube" style="width: 35px; height:35px">
            </div>
            <div><img src="../../assets/loghi/footer-pinterest.png" alt="Logo Pinterest"
                    style="width: 35px; height:35px"></div>
            <div><img src="../../assets/loghi/footer-periscope.png" alt="Logo Periscope"
                    style="width: 35px; height:35px"></div>
        </div>

    </div>

</template>

<script>
    export default {
        name: 'FooterBottom'
    }
</script>

<style lang="scss" scoped>
    @import '../../style/variabili.scss';
    @import '../../style/mixin.scss';

    #container {
        @include flex(row, space-between, center);
        padding: 20px 0;
    }

    .button {
        border: 3px solid $blue;
        cursor: pointer;

        div {
            text-transform: uppercase;
            padding: 10px;
            color: white
        }
    }

    .block-right {
        @include flex(row, initial, center);

        div {
            margin: 0 10px;
            cursor: pointer;

            span {
                @include boldUppercase();
                color: $blue;
            }
        }

    }
</style>