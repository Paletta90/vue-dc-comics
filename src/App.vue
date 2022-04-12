<template>

  <div id="app">

    <header>

      <div class="center-80">
        <LogoComp />
        <NavComp />
      </div>

    </header>

    <main>

      <div class="bg-black">
        <div class="center-80">
          <SectionContent />
        </div>
      </div>

      <div class="bg-blue">
        <div class="center-80 ">
          <SectionLink />
        </div>
      </div>

    </main>

  </div>

</template>

<script>
  // Lista di import
  import LogoComp from './components/header/LogoComp.vue'
  import NavComp from './components/header/NavComp.vue'
  import SectionContent from './components/main/SectionContent.vue'
  import SectionLink from './components/main/SectionLink.vue'

  export default {
    name: 'App',
    components: {
      LogoComp,
      NavComp,
      SectionContent,
      SectionLink
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

      div {
        padding: 10px 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }
    }

    // Utility
    .center-80 {
      width: 80%;
      margin: 0 auto;
    }

    .bg-black {
      background-color: black;
    }
    .bg-blue{
      background-color: #0282f9;
    }
  }
</style>