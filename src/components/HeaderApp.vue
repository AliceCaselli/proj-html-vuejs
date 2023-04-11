<script>
import HeadBarItem from './HeadBarItem.vue';
import HeadNavItem from './HeadNavItem.vue';


export default {

    name: 'HeaderApp',
    data() {
        return {

        };
    },

    components: {
        HeadBarItem,
        HeadNavItem,
    }
};

</script>

<template>
    <!-- upbar item  -->
    <HeadBarItem></HeadBarItem>

    <!-- logo and banner  -->
    <header>

        <div class="logo">
            <img src="img/anime-logo-300x89.webp" alt="logo">
        </div>

        <img src="img/header-banner.webp" alt="banner">

    </header>

    <!-- navbar item  -->
    <HeadNavItem></HeadNavItem>
</template>

<style lang="scss" scoped>
header {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 0;

    .logo {
        height: 100%;

        img {
            height: 65px;
        }
    }
}
</style>