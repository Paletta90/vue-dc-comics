<template>
    <div id="container">
        <h1>Content goes here</h1>
    </div>
</template>

<script>
    export default {
        name: 'SectionContent'
    }
</script>

<style lang="scss" scoped>
    @import '../../style/variabili.scss';
    @import '../../style/mixin.scss';

    #container {
        @include center-x(80%);
        padding: 50px 0;
    }

    h1 {
        color: white;
    }
</style>