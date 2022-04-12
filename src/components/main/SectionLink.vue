<template>
    <ul>
        <li v-for="(elem, index) in arrayObj" :key="index">
            <img :src="`../../assets/loghi/${elem.img}`" alt="">
            {{elem.name}}
        </li>
    </ul>
</template>

<script>
    export default{
        name: 'SectionLink',

        data(){
            return{
                arrayObj:[
                    {
                        name:'digital comics',
                        img: 'buy-comics-digital-comics.png',
                    },
                    {
                        name:'dc merchandise',
                        img: 'buy-comics-merchandise.png',
                    },
                    {
                        name:'subscription',
                        img: 'buy-comics-subscriptions.png',
                    },
                    {
                        name:'comic shop locator',
                        img: 'buy-comics-shop-locator.png',
                    },
                    {
                        name:'dc power visa',
                        img: 'buy-dc-power-visa.svg',
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../style/mixin.scss';

    ul{
        // Lista in flex e style-type:none
        @include listHorizontal();
        padding: 30px 0;

        li{
            margin: 0 10px;
            text-transform: uppercase;
            font-size: 0.8rem;
            color: white;
            display: flex;
            align-items: center;

            img{
                width: 50px;
                margin: 0 10px;
            }
        }
    }
</style>