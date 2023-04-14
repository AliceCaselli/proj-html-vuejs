<script>

export default {

    name: 'ThumbItem',
    data() {
        return {};
    },

    props: {
        thumb: Object,
        index: Number,
    }
};

</script>

<template>
    <div class="thumb-item">
        <img :src="thumb.image" alt="" @click="$emit('active')">

        <div class="text">
            <div class="first-row">

                <span class="user"><i class="fa-solid fa-user"></i>{{ thumb.user }}</span>
                <span class="date"><i class="fa-solid fa-calendar-days"></i>{{ thumb.date }}</span>
            </div>
            <div class="title">{{ thumb.title }}</div>
        </div>

        <button>{{ thumb.button }}</button>
    </div>
</template>

<style lang="scss" scoped>
.thumb-item {
    height: calc(100% / 3);

    display: flex;
    flex-direction: row;
    align-items: center;
    border-bottom: 2px solid #33333360;

    position: relative;

    &:last-child {
        border-bottom: none;
    }

    img {
        height: 80%;
        width: 60%;
        object-fit: cover;
        filter: brightness(.6);

        &:hover {
            filter: brightness(1);
            cursor: pointer;
        }
    }

    .text {
        width: 100%;

        display: flex;
        flex-direction: column;
        justify-content: center;
        font-size: .8em;
        padding: 0 10px;

        .first-row {
            width: 100%;
            display: flex;
            flex-direction: row;
            gap: 10px;

            .user,
            .date {
                display: flex;
                flex-direction: row;
                gap: 5px;
                align-items: baseline;
            }
        }

        .title {
            font-weight: bold;
        }
    }


    button {
        position: absolute;
        top: 20px;
        left: 15px;

        background-color: #fff;
        border-color: transparent;
        color: #333333;
        border-radius: 5px;
        padding: 0 5px;
    }
}
</style>