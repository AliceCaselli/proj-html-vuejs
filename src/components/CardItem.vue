<script>

export default {

    name: 'CardItem',
    data() {
        return {

        };
    },

    props: {
        card: Object,
    }
};

</script>

<template>
    <div class="card">
        <div class="card-img">
            <img :src="card.img" alt="">
        </div>
        <div class="card-text">
            <div class="card-title">{{ card.title }}</div>
            <div class="card-date">{{ card.date }}</div>
            <div class="card-description">{{ card.text }}</div>

            <div class="read-more-btn">
                <button>Read More</button>
            </div>

        </div>
        <div class="card-btn">
            <button v-for="button in card.buttons">{{ button }}</button>
        </div>

    </div>
</template>

<style lang="scss" scoped>
.card {

    position: relative;
    width: calc(100% / 3);

    .card-img {
        height: 300px;

        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
        }
    }

    .card-text {
        background-color: #f3f3f3;
        text-align: center;
        padding: 20px 0;

        .card-title {
            font-weight: bold;
        }

        .card-description {
            padding: 0 20px;
            font-size: 0.9em;
            margin: 10px 0;
        }

        .read-more-btn {
            button {
                background-color: #bf1d2e;
                border-color: transparent;
                border-radius: 30px;
                padding: 5px 25px;
            }
        }
    }

    .card-btn {
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