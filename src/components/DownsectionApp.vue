<script>

import CardshowApp from './CardshowApp.vue';
import VideolistApp from './VideolistApp.vue';

export default {

    name: 'DownsectionApp',
    data() {
        return {};
    },

    components: {
        CardshowApp,
        VideolistApp,
    }
};

</script>

<template>
    <div class="bg-color">
        <div class="container-downsection">

            <div class="title-break">

                <h2>FEATURED POSTS</h2>
                <div class="icons-title-break">
                    <i class="fa-solid fa-chevron-left"></i>
                    <i class="fa-solid fa-chevron-right"></i>
                </div>
            </div>

            <CardshowApp></CardshowApp>
            <VideolistApp></VideolistApp>

        </div>
    </div>
</template>

<style lang="scss" scoped>
.bg-color {

    background-color: white;

    .container-downsection {

        max-width: 1200px;
        margin: 0 auto;
        padding: 60px 0;

        .title-break {
            display: flex;
            flex-direction: row;
            justify-content: space-between;
            align-items: center;

            .icons-title-break {
                display: flex;
                flex-direction: row;
                gap: 20px;

                .fa-solid {
                    height: 35px;
                    width: 35px;
                    display: flex;
                    flex-direction: row;
                    justify-content: center;
                    align-items: center;
                    background-color: #333333;
                    color: white;
                    border-radius: 50%;
                }
            }
        }
    }
}
</style>