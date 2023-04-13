<script>

export default {

    name: 'SquareItem',
    data() {
        return {

        };
    },

    props: {
        square: Object,
    }
};

</script>

<template>
    <div class="square">

        <img :src="square.img" alt="">

        <div class="category">{{ square.category }}</div>

    </div>
</template>

<style lang="scss" scoped>
.square {
    position: relative;
    height: 240px;
    width: calc(100% / 6 - 5px * 5);

    img {
        height: 100%;
        width: 100%;
        object-fit: cover;
        filter: brightness(.8);
        border-radius: 5px;
    }

    .category {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: white;
        font-weight: bold;
    }
}
</style>