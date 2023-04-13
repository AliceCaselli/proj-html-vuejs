<script>

import UpfooterApp from './UpfooterApp.vue';
import DownfooterApp from './DownfooterApp.vue';

export default {

    name: 'FooterApp',
    data() {
        return {};
    },

    components: {
        UpfooterApp,
        DownfooterApp,
    }
};

</script>

<template>
    <div class="bg-color">

        <div class="container-footer">

            <UpfooterApp></UpfooterApp>
            <DownfooterApp></DownfooterApp>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.bg-color {
    background-color: #bf1d2e;
    border-top: 4px solid #333333;

    color: white;

    .container-footer {
        max-width: 1200px;
        margin: 0 auto;
    }
}
</style>