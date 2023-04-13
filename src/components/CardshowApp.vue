<script>

import CardItem from './CardItem.vue';

export default {

    name: 'CardshowApp',
    data() {
        return {
            cards: [
                {
                    img: 'img/ideas-anime.webp',
                    title: 'Live Ideas Might Be Anime',
                    date: 'December 26, 2022',
                    buttons: [
                        'Culture',
                        'Stories',
                    ],
                    text: 'lorem ipsum dolor sit amet, conse ctetur adipiscing elit. Sed maximus orci ac condi mentum...'

                },
                {
                    img: 'img/visit-france.webp',
                    title: 'Reasons To Visit France',
                    date: 'December 26, 2022',
                    buttons: [
                        'Lifestyle',
                        'Travel',
                    ],
                    text: 'lorem ipsum dolor sit amet, conse ctetur adipiscing elit. Sed maximus orci ac condi mentum...'

                },
                {
                    img: 'img/travel-alone.webp',
                    title: 'Traveling Alone Is Awesome',
                    date: 'December 26, 2022',
                    buttons: [
                        'Stories',
                        'Travel',
                    ],
                    text: 'lorem ipsum dolor sit amet, conse ctetur adipiscing elit. Sed maximus orci ac condi mentum...'

                },

            ]
        };
    },

    components: {
        CardItem,
    }
};

</script>

<template>
    <div class="container-cards">

        <CardItem v-for="card in cards" :card="card"></CardItem>
    </div>
</template>

<style lang="scss" scoped>
.container-cards {
    display: flex;
    flex-direction: row;
    gap: 10px;
    margin-top: 20px
}
</style>