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
            ]
        };
    },

    components: {
        SlideItem,
    }
};

</script>

<template>
    <div class="container-slideshow">

        <SlideItem v-for="slide in slides" :slide="slide"></SlideItem>
    </div>
</template>

<style lang="scss" scoped>
.container-slideshow {
    display: flex;
    flex-direction: row;
    margin: 30px;
    gap: 10px
}
</style>