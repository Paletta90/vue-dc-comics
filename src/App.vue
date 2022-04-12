<template>

  <div id="app">

    <!-- header -->
    <header>

      <div class="center-80">

        <LogoComp />
        <NavComp />

      </div>

    </header>

    <!-- Main -->
    <main>

      <!-- Sezione da riempire -->
      <section class="bg-black">

        <div class="center-80">

          <SectionContent />

        </div>

      </section>

      <!-- Sezione blu  -->
      <section class="bg-blue">

        <div class="center-80 ">

          <SectionLink />

        </div>

      </section>

    </main>

    <!-- Footer -->
    <footer>

      <!-- Background con immagine -->
      <section class="bg-footerImg">

        <div class="center-80">

          <FooterLink />
          <div>
            <FooterImg />
          </div>
          

        </div>

      </section>

      <section class="bg-footer">
        <div class="center-80">
          <FooterBottom />
        </div>
      </section>

    </footer>

  </div>

</template>

<script>
  // Lista di import
  import LogoComp from './components/header/LogoComp.vue'
  import NavComp from './components/header/NavComp.vue'
  import SectionContent from './components/main/SectionContent.vue'
  import SectionLink from './components/main/SectionLink.vue'
  import FooterLink from './components/footer/FooterLink.vue'
  import FooterImg from './components/footer/FooterImg.vue'
  import FooterBottom from './components/footer/FooterBottom.vue'

  export default {
    name: 'App',
    components: {
      LogoComp,
      NavComp,
      SectionContent,
      SectionLink,
      FooterLink,
      FooterImg,
      FooterBottom
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

    footer section:nth-child(1) > div{
      position: relative;
      display: flex;
    }
    
    // Utility
    .center-80 {
      width: 80%;
      margin: 0 auto;
    }

    .bg-black {
      background-color: black;
    }

    .bg-blue {
      background-color: #0282f9;
    }

    .bg-footerImg {
      background-image: url('./assets/img/footer-bg.jpg');
    }
    
    .bg-footer{
      background-color: #303030;
    }
  }
</style>