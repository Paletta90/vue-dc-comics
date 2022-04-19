<template>

  <div id="app">

    <!-- header -->
    <header>

      <NavComp />

    </header>

    <!-- Main -->
    <main>

      <!-- Sezione jumbotron e movies -->
      <section class="bg-black">

        <SectionJumbotron />
        <SectionContent />

      </section>

      <!-- Sezione blu  -->
      <section class="bg-blue">

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
      <section class="bg-footer">

        <FooterBottom />

      </section>

    </footer>

  </div>

</template>

<script>
  // Lista di import
  import NavComp from './components/header/NavComp.vue'
  import SectionJumbotron from './components/main/SectionJumbotron.vue'
  import SectionContent from './components/main/SectionContent.vue'
  import SectionLink from './components/main/SectionLink.vue'
  import FooterLink from './components/footer/FooterLink.vue'
  import FooterBottom from './components/footer/FooterBottom.vue'

  export default {
    name: 'App',
    components: {
      NavComp,
      SectionJumbotron,
      SectionContent,
      SectionLink,
      FooterLink,
      FooterBottom
    }
  }
</script>

<style lang="scss">
  @import './style/utility.scss';
  @import './style/variabili.scss';
  @import './style/mixin.scss';

  // Reset del body
  * {
    @include reset();
  }


  #app {
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
 
  // General
  a {
    text-decoration: none;
  }

  #container {
    @include center-x(80%);
  }
</style>