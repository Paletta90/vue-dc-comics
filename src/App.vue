<template>

  <div id="app">

    <header>
      <div>
        <LogoComp />
        <NavComp />
      </div>
    </header>

  </div>

</template>

<script>
  // Lista di import
  import LogoComp from './components/header/LogoComp.vue'
  import NavComp from './components/header/NavComp.vue'

  export default {
    name: 'App',
    components: {
      LogoComp,
      NavComp
    }
  }
</script>

<style lang="scss">
  @import './style/variabili.scss';

  // Reset del body
  * {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  #app {
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;

    // Header
    header {
      background-color: $bg-header;

      div{
        width: 80%;
        margin: 0 auto;
        padding: 10px 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }
    }
  }
</style>