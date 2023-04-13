<script>

import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import SlideshowApp from './components/SlideshowApp.vue';
import SquareshowApp from './components/SquareshowApp.vue';
import FooterApp from './components/FooterApp.vue';
export default {
  data() {
    return {};
  },

  components: {
    HeaderApp,
    MainApp,
    SlideshowApp,
    SquareshowApp,
    FooterApp,
  }
};

</script>

<template>
  <HeaderApp></HeaderApp>
  <SlideshowApp></SlideshowApp>
  <MainApp></MainApp>
  <SquareshowApp></SquareshowApp>
  <FooterApp></FooterApp>
</template>

<style lang="scss" scoped></style>