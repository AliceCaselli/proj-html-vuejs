<script>

export default {

    name: 'SlideItem',
    data() {
        return {

        };
    },

    props: {
        slide: Object,
        index: Number,
        activeIndex: Number,
        slideNumber: Number,
    }
};

</script>

<template>
    <div v-if="(index >= activeIndex) && (index <= activeIndex + slideNumber)" class="slide-card">
        <div class="slide-img">
            <img :src="slide.img" alt="">
        </div>
        <div class="slide-text">
            <div class="slide-title">{{ slide.title }}</div>
            <div class="slide-date">{{ slide.date }}</div>
        </div>
        <div class="slide-btn">
            <button v-for="button in slide.buttons">{{ button }}</button>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.slide-card {

    position: relative;
    width: calc(100% / 4);


    .slide-img {
        height: 300px;

        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
        }
    }

    .slide-text {
        background-color: #fff;
        text-align: center;
        padding: 10px 0;

        .slide-title {
            font-weight: bold;
        }
    }

    .slide-btn {
        position: absolute;
        top: 10px;
        left: 50%;
        transform: translateX(-50%);
        display: flex;
        flex-direction: row;
        gap: 10px;


        button {
            background: white;
            border-color: transparent;
            border-radius: 5px;
            color: #333333;
            font-weight: bold;
            padding: 2px 8px;
        }
    }


}
</style>