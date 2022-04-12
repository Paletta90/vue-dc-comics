<template>

    <div class="cont-flex">

        <span class="button">
            <div>sign-up now!</div>
        </span>

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

    @import '../../style/mixin.scss';

    .cont-flex {
        @include flex(row, space-between, center);
        padding: 20px 0;
        color: #057be8;
    }

    .button {
        border: 3px solid #057be8;

        div {
            text-transform: uppercase;
            padding: 10px;
        }
    }

    .block-right {
        display: flex;
        align-items: center;

        div {
            margin: 0 10px;

            span {
                text-transform: uppercase;
                font-weight: bold;
            }
        }

    }
</style>