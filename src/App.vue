<script>

import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import SlideshowApp from './components/SlideshowApp.vue';
export default {
  data() {
    return {};
  },

  components: {
    HeaderApp,
    MainApp,
    SlideshowApp
  }
};

</script>

<template>
  <HeaderApp></HeaderApp>
  <SlideshowApp></SlideshowApp>
  <MainApp></MainApp>
</template>

<style lang="scss" scoped></style>