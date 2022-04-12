<template>
    <ul>
        <li v-for="(elem, index) in arrayObj" :key="index">{{elem.name}}</li>
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
                        img: '',
                    },
                    {
                        name:'dc merchandise',
                        img: '',
                    },
                    {
                        name:'subscription',
                        img: '',
                    },
                    {
                        name:'comic shop locator',
                        img: '',
                    },
                    {
                        name:'dc power visa',
                        img: '',
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

        li{
            margin: 0 10px;
            text-transform: uppercase;
            font-size: 0.9rem;
            color: white;

        }
    }
</style>