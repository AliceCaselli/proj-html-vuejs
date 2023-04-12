<script>

import ShowItem from './ShowItem.vue';

export default {

    name: 'ShowtableApp',
    data() {
        return {
            items: [
                {
                    image: 'img/anime-fashion.webp',
                    buttons: [
                        'Fashion',
                        'Lifestyle',
                    ],
                    user: 'demo',
                    date: 'December 25, 2022',
                    title: 'Fashion Trend Now A Days',
                },
                {
                    image: 'img/travel-alone.webp',
                    buttons: [
                        'Stories',
                        'Travel',
                    ],
                    user: 'demo',
                    date: 'December 26, 2022',
                    title: 'Traveling Alone Is Awesome',
                },
                {
                    image: 'img/best-places.webp',
                    buttons: [
                        'Lifestyle',
                        'Stories',
                        'Travel',
                    ],
                    user: 'demo',
                    date: 'December 25, 2022',
                    title: 'Places For A Road Trip',
                },
                {
                    image: 'img/music-love.webp',
                    buttons: [
                        'Culture',
                        'Lifestyle',
                    ],
                    user: 'demo',
                    date: 'December 25, 2022',
                    title: 'Music The Love Of My Life',
                },
                {
                    image: 'img/visit-france.webp',
                    buttons: [
                        'Lifestyle',
                        'Travel',
                    ],
                    user: 'demo',
                    date: 'December 26, 2022',
                    title: 'Reasons To Visit France',
                }
            ]
        };
    },

    components: {
        ShowItem,
    }
};

</script>

<template>
    <div class="table">
        <ShowItem v-for="item in items" :item="item"></ShowItem>
    </div>
</template>

<style lang="scss" scoped>
.table {
    max-width: 1200px;
    margin: 0 auto;
    height: 450px;
    display: flex;
    flex-flow: column wrap;
    gap: 10px;
    justify-content: space-between;

}
</style>