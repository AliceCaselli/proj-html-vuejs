<script>

export default {

    name: 'HeadNavItem',
    data() {
        return {};
    },
};

</script>

<template>
    <nav>

        <div class="container-nav">

            <div class="menu">
                <i class="fa-solid fa-bars"></i>
            </div>

            <div class="links">
                <ul>
                    <li><a href="#">
                            <i class="fa-solid fa-house-chimney"></i>HOME</a></li>
                </ul>
            </div>

            <div class="search">
                <i class="fa-solid fa-magnifying-glass"></i>
            </div>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
nav {
    background-color: #ffffff;

    height: 50px;

    .container-nav {
        height: 100%;
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }


    .fa-solid {
        color: #333333;
    }
}
</style>