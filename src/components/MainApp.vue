<script>

import UpsectionApp from './UpsectionApp.vue';

export default {

    name: 'MainApp',
    data() {
        return {};
    },

    components: {
        UpsectionApp,
    }
};

</script>

<template>
    <div class="bg-color">

        <div class="container-main">

            <UpsectionApp></UpsectionApp>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.bg-color {
    background-color: white;

    .container-main {
        max-width: 1200px;
        margin: 0 auto;
        padding-top: 60px;
    }
}
</style>