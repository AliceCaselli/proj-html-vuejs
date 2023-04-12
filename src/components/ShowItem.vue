<script>

export default {

    name: 'ShowItem',
    data() {
        return {

        };
    },

    props: {
        item: Object,

    }
};

</script>

<template>
    <div class="item">

        <img :src="item.image" alt="">
        <div class="btn-item">

            <button v-for="button in item.buttons">{{ button }}</button>
        </div>
        <div class="text">

            <div class="first-row">

                <span class="user"><i class="fa-solid fa-user"></i>{{ item.user }}</span>
                <span class="date"><i class="fa-solid fa-calendar-days"></i>{{ item.date }}</span>
            </div>
            <div class="title">{{ item.title }}</div>

        </div>
    </div>
</template>

<style lang="scss" scoped>
.item {
    position: relative;
    height: calc(100% / 2 - 5px);
    width: calc(100% / 4);


    &:nth-child(3) {
        height: 100%;
        width: calc(100% / 2);
    }

    img {
        height: 100%;
    }

    .btn-item {
        position: absolute;
        display: flex;
        flex-direction: row;
        gap: 10px;
        left: 50%;
        transform: translateX(-50%);
        top: 20px;

        button {
            background-color: #fff;
            border: transparent;
            color: #333333;
            padding: 5px;
        }
    }

    .text {
        position: absolute;
        width: 100%;


        z-index: 2;
        bottom: 25px;
        color: white;

        display: flex;
        flex-direction: column;
        align-items: center;

        .first-row {
            width: 100%;
            display: flex;
            flex-direction: row;
            justify-content: center;
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
}
</style>