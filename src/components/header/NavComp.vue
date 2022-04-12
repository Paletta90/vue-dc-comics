<template>
    
    <ul>
        <li v-for="(elem, index) in navBar" :key="index">{{elem}}</li>
    </ul>

</template>

<script>
    export default{
        name: 'NavComp',

        data(){
            return{
                navBar:[
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

    @import '../../style/mixin.scss';

    ul{
        // Lista in flex e style-type:none
        @include listHorizontal();

        li{
            margin: 0 10px;
            // Stile bold e uppercase
            @include boldUppercase();
            font-size: 0.7rem;

        }
    }
</style>