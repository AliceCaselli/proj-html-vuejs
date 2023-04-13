<script>

export default {

    name: 'Slidethumb',
    data() {
        return {};
    },
};

</script>

<template>
    <div class="container-slide">

        <div class="slide-active">
            <img src="img/success-story.webp" alt="">
        </div>
        <div class="thumb"></div>
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
        }
    }

    .thumb {
        height: 450px;
        width: 500px;
        background-color: blue;
    }
}
</style>