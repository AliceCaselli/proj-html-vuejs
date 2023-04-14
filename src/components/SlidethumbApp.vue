<script>

import ThumbItem from './ThumbItem.vue';

export default {

    name: 'Slidethumb',
    data() {
        return {

            thumbs: [

                {
                    image: 'img/success-story.webp',
                    button: 'Stories',
                    user: 'demo',
                    date: 'December 26, 2022',
                    title: 'Traveling Alone Is Awesome',
                },
                {
                    image: 'img/travel-alone.webp',
                    button: 'Stories',
                    user: 'demo',
                    date: 'December 26, 2022',
                    title: 'Traveling Alone Is Awesome',
                },
                {
                    image: 'img/best-places.webp',
                    button: 'Lifestyle',
                    user: 'demo',
                    date: 'December 25, 2022',
                    title: 'Places For A Road Trip',
                },
                {
                    image: 'img/music-love.webp',
                    button: 'Culture',
                    user: 'demo',
                    date: 'December 25, 2022',
                    title: 'Music The Love Of My Life',
                },
            ],

            activeIndex: 0,
        };
    },

    components: {
        ThumbItem,
    },

    methods: {

        activeImg(clickIndex) {

            this.activeIndex = clickIndex;
        }

    }

};

</script>

<template>
    <div class="container-slide">

        <div class="slide-active">
            <img :src="this.thumbs[activeIndex].image" alt="">
        </div>
        <div class="thumbs">
            <ThumbItem v-for="(thumb, index) in thumbs" :thumb="thumb" :index="index" @active="activeImg(index)">
            </ThumbItem>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container-slide {

    margin-top: 30px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    .slide-active {
        // width: 450px;
        height: 450px;

        img {
            height: 100%;
            filter: brightness(.6);
        }
    }

    .thumbs {
        height: 450px;
        width: calc(100% - 700px);
        overflow-y: scroll;
    }
}
</style>