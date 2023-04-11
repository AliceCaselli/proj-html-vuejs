<script>

export default {

    name: 'HeadBarItem',
    data() {
        return {};
    },


};

</script>

<template>
    <div class="upbar">
        <div class="container-upbar">

            <div class="left-bar">
                <button>NEWS UPDATES</button>
                <img src="/img/meal-time-150x150.webp" alt="">
                <span>5:35 THE_</span>
            </div>

            <div class="right-bar">
                <i class="fa-solid fa-chevron-left"></i>
                <i class="fa-solid fa-chevron-right"></i>

                <div class="icons">
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-twitter"></i>
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-youtube"></i>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
//total background
.upbar {
    height: 40px;
    background-color: #bf1d2e;

    .container-upbar {
        height: 100%;

        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
    }

    //button + img
    .left-bar {
        display: flex;
        flex-direction: row;
        height: 100%;
        background-color: green;

        span {
            align-self: center;
            font-weight: bold;
            padding: 0 5px;
        }
    }

    .right-bar {
        height: 100%;
        background-color: blue;
    }
}
</style>