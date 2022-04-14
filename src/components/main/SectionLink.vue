<template>
    <div id="container">
        <ul>
            <li v-for="(elem, index) in arrayObj" :key="index">
                <img :src="elem.img" alt="">
                {{elem.name}}
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
                        img: require('../../assets/loghi/buy-comics-digital-comics.png'),
                    },
                    {
                        name: 'dc merchandise',
                        img: require('../../assets/loghi/buy-comics-merchandise.png'),
                    },
                    {
                        name: 'subscription',
                        img: require('../../assets/loghi/buy-comics-subscriptions.png'),
                    },
                    {
                        name: 'comic shop locator',
                        img: require('../../assets/loghi/buy-comics-shop-locator.png'),
                    },
                    {
                        name: 'dc power visa',
                        img: require('../../assets/loghi/buy-dc-power-visa.svg'),
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
        @include center-x(80%);
        padding: 30px 0;
    }

    ul {
        // Lista in flex e style-type:none
        @include listHorizontal();

        li {
            margin: 0 10px;
            text-transform: uppercase;
            font-size: $f-medium;
            color: white;
            @include flex(row, initial, center);

            img {
                width: 50px;
                margin: 0 10px;
            }
        }
    }
</style>