<template>
    <div id="container">
        <ul>
            <li v-for="(elem, index) in arrayObj" :key="index">
                <a href="#">
                    <img :src= "require(`../../assets/loghi/${elem.img}`)" alt="">
                    {{elem.name}}
                </a>
            </li>
        </ul>
    </div>

</template>

<script>
    export default {
        name: 'SectionLink',

        data() {
            return {
                arrayObj: [{
                        name: 'digital comics',
                        img: 'buy-comics-digital-comics.png'
                    },
                    {
                        name: 'dc merchandise',
                        img: 'buy-comics-merchandise.png'
                    },
                    {
                        name: 'subscription',
                        img: 'buy-comics-subscriptions.png'
                    },
                    {
                        name: 'comic shop locator',
                        img: 'buy-comics-shop-locator.png'
                    },
                    {
                        name: 'dc power visa',
                        img: 'buy-dc-power-visa.svg'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../style/variabili.scss';
    @import '../../style/mixin.scss';

    #container {
        padding: 30px 0;


        ul {
            // Lista in flex e style-type:none
            @include listHorizontal();

            li {
                margin: 0 10px;
                @include flex(row, initial, center);

                a {
                    @include flex(row, initial, center);
                    color: white;
                    text-transform: uppercase;
                    font-size: $f-medium;
                }

                img {
                    width: 50px;
                    margin: 0 10px;
                }
            }
        }
    }
</style>