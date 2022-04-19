<template>

    <div id="container">

        <div>
            <a href="#">
                <img src="../../assets/loghi/dc-logo.png" alt="Logo DC" width="50px">
            </a>
        </div>

        <ul>
            <li v-for="(elem, index) in navBar" :key="index">
                <a href="#">
                    <div class="p-yb-30">{{elem}}</div>
                </a>
                <div class="bar"></div>
            </li>
        </ul>

    </div>


</template>

<script>
    export default {
        name: 'NavComp',

        data() {
            return {
                navBar: [
                    'characters',
                    'comics',
                    'movies',
                    'tv',
                    'games',
                    'collectibles',
                    'videos',
                    'fans',
                    'news',
                    'shop'
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../style/variabili.scss';
    @import '../../style/mixin.scss';

    #container {
        @include flex(row, space-between, center);

        ul {
            padding-top: 30px;
            // Lista in flex e style-type:none
            @include listHorizontal();

            li {
                cursor: pointer;
                margin: 0 10px;
                @include boldUppercase();
                @include flex(column, space-between, initial);

                a {
                    font-size: $f-small;
                    color: black;
                }

                &:hover {
                    color: $blue;

                    .bar {
                        background-color: $blue;
                    }
                }
            }
        }
    }

    // Barra per l'effetto all hover
    .bar {
        width: 100%;
        height: 5px;
    }

    .p-yb-30 {
        padding-bottom: 30px;
    }
</style>