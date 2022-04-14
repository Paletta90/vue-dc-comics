<template>

  <div id="app">

    <!-- header -->
    <header>

        <NavComp />

    </header>

    <!-- Main -->
    <main>

      <!-- Sezione da riempire -->
      <section class="bg-black">

          <SectionContent />

      </section>

      <!-- Sezione blu  -->
      <section class="bg-blue z-index-1">

          <SectionLink />

      </section>

    </main>

    <!-- Footer -->
    <footer>

      <!-- Background con immagine -->
      <section class="bg-footerImg">

          <FooterLink />

      </section>

      <!-- Sezione finale -->
      <section class="bg-footer z-index-1">

          <FooterBottom />

      </section>

    </footer>

  </div>

</template>

<script>
  // Lista di import
  import NavComp from './components/header/NavComp.vue'
  import SectionContent from './components/main/SectionContent.vue'
  import SectionLink from './components/main/SectionLink.vue'
  import FooterLink from './components/footer/FooterLink.vue'
  import FooterBottom from './components/footer/FooterBottom.vue'

  export default {
    name: 'App',
    components: {
      NavComp,
      SectionContent,
      SectionLink,
      FooterLink,
      FooterBottom
    }
  }
</script>

<style lang="scss">
  @import './style/variabili.scss';
  @import './style/mixin.scss';

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

    // Utility
    .bg-black {
      background-color: black;
    }

    .bg-blue {
      background-color: $blue;
    }

    .bg-footerImg {
      background-image: url('./assets/img/footer-bg.jpg');
    }

    .bg-footer {
      background-color: #303030;
    }
    .z-index-1{
      position: relative;
      z-index: 1;
    }
  }

  // General
  a{
    text-decoration: none;
  }

  #container{
    @include center-x(80%);
  }

</style>