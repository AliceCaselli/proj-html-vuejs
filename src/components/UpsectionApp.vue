<script>

import ShowtableApp from './ShowtableApp.vue';
import SlidethumbApp from './SlidethumbApp.vue';

export default {

    name: 'UpsectionApp',
    data() {
        return {};
    },

    components: {
        ShowtableApp,
        SlidethumbApp,
    }
};

</script>

<template>
    <div class="bg-color">
        <div class="container-upsection">

            <ShowtableApp></ShowtableApp>
            <div class="title-break">

                <h2>LIFESTYLE & STORIES</h2>
                <div class="btn-title-break">
                    <button>ALL</button>
                    <button>LIFESTYLE</button>
                    <button>STORIES</button>
                </div>
            </div>

            <SlidethumbApp></SlidethumbApp>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.bg-color {

    background-color: white;

    .container-upsection {

        max-width: 1200px;
        margin: 0 auto;
        padding: 60px 0;

        .title-break {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;

            .btn-title-break {
                display: flex;
                flex-direction: row;
                gap: 20px;

                button {
                    padding: 5px 10px;
                    background: #333333;
                    border: transparent;
                    border-radius: 5px;
                }
            }
        }
    }
}
</style>