<script>

import SquareItem from './SquareItem.vue';

export default {

    name: 'SquareshowApp',
    data() {
        return {
            squares: [
                {
                    img: 'img/anime-fashion.webp',
                    category: 'FASHION',
                },
                {
                    img: 'img/success-story.webp',
                    category: 'CULTURE',
                },
                {
                    img: 'img/healthy-foods.webp',
                    category: 'FOOD',
                },
                {
                    img: 'img/visit-france.webp',
                    category: 'LIFESTYLE',
                },
                {
                    img: 'img/travel-alone.webp',
                    category: 'STORIES',
                },
                {
                    img: 'img/best-places.webp',
                    category: 'TRAVEL',
                },
            ]
        };
    },

    components: {
        SquareItem,
    }
};

</script>

<template>
    <div class="bg-color">

        <div class="container-squares">

            <SquareItem v-for="square in squares" :square="square"></SquareItem>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.bg-color {
    background-color: #fff;
    margin-bottom: 10px;

    .container-squares {
        padding: 0 10px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }
}
</style>