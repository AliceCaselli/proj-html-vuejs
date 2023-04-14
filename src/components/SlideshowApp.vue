<script>

import SlideItem from './SlideItem.vue';

export default {

    name: 'SlideshowApp',
    data() {
        return {
            slides: [
                {
                    img: 'img/healthy-foods.webp',
                    title: 'The Best Healthy Foods In 2022',
                    date: 'December 26, 2022',
                    buttons: [
                        'Food',
                    ],
                },
                {
                    img: 'img/winter.webp',
                    title: 'The Best Winter Outfits',
                    date: 'December 26, 2022',
                    buttons: [
                        'Fashion',
                    ],
                },
                {
                    img: 'img/photographers-mistakes.webp',
                    title: "Beginner Photographer's Mistakes",
                    date: 'December 26, 2022',
                    buttons: [
                        'Fashion',
                    ],
                },
                {
                    img: 'img/ideas-anime.webp',
                    title: 'Live Ideas Might Be Anime',
                    date: 'December 26, 2022',
                    buttons: [
                        'Culture',
                        'Stories',
                    ],
                },
                {
                    img: 'img/music-love.webp',
                    title: 'Music The Love Of My Life',
                    date: 'December 26, 2022',
                    buttons: [
                        'Culture',
                        'Lifestyle',
                    ],
                },
                {
                    img: 'img/anime-fashion.webp',
                    title: 'Fashion Trend Now A Days',
                    date: 'December 26, 2022',
                    buttons: [
                        'Fashion',
                        'Lifestyle',
                    ],
                },

            ],

            activeIndex: 0,

            slideNumber: 3,

        };
    },

    components: {
        SlideItem,
    },

    methods: {

        slideShowNext() {

            this.activeIndex++;

            if (this.activeIndex + this.slideNumber == this.slides.length) {

                this.activeIndex = 0;
            }

        },

        slideShowPrev() {

            this.activeIndex--;

            if (this.activeIndex < 0) {

                this.activeIndex = this.slides.length - 1 - this.slideNumber;
            }


        }
    }


};

</script>

<template>
    <div class="container-slideshow">

        <i class="fa-solid fa-chevron-left" @click="slideShowPrev()"></i>
        <SlideItem v-for="(slide, index) in slides" :slide="slide" :index="index" :activeIndex="activeIndex"
            :slideNumber="slideNumber"></SlideItem>
        <i class="fa-solid fa-chevron-right" @click="slideShowNext()"></i>
    </div>
</template>

<style lang="scss" scoped>
.container-slideshow {
    display: flex;
    flex-flow: row nowrap;
    margin: 30px;
    gap: 10px;

    position: relative;

    .fa-solid {
        z-index: 1;
        position: absolute;
        background-color: #fff;
        height: 30px;
        width: 30px;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        opacity: .8;
    }

    .fa-chevron-left {
        top: 50%;
        transform: translateY(-50%);
        left: 20px;

    }

    .fa-chevron-right {
        top: 50%;
        transform: translateY(-50%);
        right: 20px;

    }
}
</style>