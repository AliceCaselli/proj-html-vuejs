<script>

import UpsectionApp from './UpsectionApp.vue';
import DownsectionApp from './DownsectionApp.vue';

export default {

    name: 'MainApp',
    data() {
        return {};
    },

    components: {
        UpsectionApp,
        DownsectionApp,
    }
};

</script>

<template>
    <UpsectionApp></UpsectionApp>

    <div class="container-break">
        <div class="banner-break">
            <img src="img/page-banner-1.webp" alt="">
        </div>
    </div>

    <DownsectionApp></DownsectionApp>
</template>

<style lang="scss" scoped>
.container-break {
    max-width: 1200px;
    margin: 30px auto;



    .banner-break {
        width: 100%;

        img {
            width: 100%;
        }
    }
}
</style>