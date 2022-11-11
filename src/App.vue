<template>
  <HeaderComponent/>
  <main>
    <HeroSection/>
    <DarkContentSection/>
    <BlueIconSection/>
  </main>
  <FooterComponent/>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import HeroSection from './components/HeroSection.vue';
import DarkContentSection from './components/DarkContentSection.vue';
import BlueIconSection from './components/BlueIconSection.vue';
import FooterComponent from './components/FooterComponent.vue';


  export default {
    components:{
      HeaderComponent,
      HeroSection,
      DarkContentSection,
      BlueIconSection,
      FooterComponent
    }
    
  }
</script>

<style lang="scss" scoped>

</style>