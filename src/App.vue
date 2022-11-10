<template>
  <HeaderComponent/>
  <DarkContentSection/>
  <BlueIconSection/>
  <FooterComponent/>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import DarkContentSection from './components/DarkContentSection.vue';
import BlueIconSection from './components/BlueIconSection.vue';
import FooterComponent from './components/FooterComponent.vue';

  export default {
    components:{
      HeaderComponent,
      DarkContentSection,
      BlueIconSection,
      FooterComponent
    }
    
  }
</script>

<style lang="scss" scoped>

</style>