<template>
    <div class="movie">
        <div class="bg-movie" :style="{ 'background-image': 'url( ' + url +  ' )' } "></div>
        <p>{{series}}</p>
    </div>
</template>

<script>
    export default {
        name: 'BoxMovie',
        // props: ['url',
        //     'series'
        // ]
        props: {
            url: String,
            series: String
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../style/variabili.scss';
    @import '../../style/mixin.scss';

    .movie {
        width: calc((100% / 6) - 10px);
        margin: 20px 5px;

        .bg-movie {
            background-size: cover;
            width: 100%;
            aspect-ratio: 1;
            margin: 10px 0;
        }

        p {
            color: white;
            text-transform: uppercase;
            font-size: $f-small;
        }

    }
</style>