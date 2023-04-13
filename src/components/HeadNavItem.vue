<script>

export default {

    name: 'HeadNavItem',
    data() {
        return {
            links: [
                {
                    icon: 'fa-solid fa-house-chimney',
                    link: 'HOME',
                },
                {
                    icon: 'fa-solid fa-suitcase',
                    link: 'LIFESTYLE',
                    chevron: 'fa-solid fa-chevron-down',

                },
                {
                    icon: 'fa-solid fa-book-open-reader',
                    link: 'STORIES',
                    chevron: 'fa-solid fa-chevron-down',

                },
                {
                    icon: 'fa-solid fa-book',
                    link: 'PAGES',
                    chevron: 'fa-solid fa-chevron-down',

                },
                {
                    icon: 'fa-solid fa-user',
                    link: 'ABOUT US',
                },
            ],
        };
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
                    <li v-for="link in links">
                        <i :class="link.icon"></i><a href="#">{{ link.link }}</a>
                        <i :class="link.chevron"></i>
                    </li>
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


        .links {
            ul {

                display: flex;
                flex-direction: row;
                gap: 30px;

                li {
                    display: flex;
                    flex-direction: row;
                    gap: 5px;
                    align-items: center;


                    a {
                        color: #333333;
                        text-decoration: none;
                    }
                }
            }

        }
    }


    .fa-solid {
        color: #333333;
    }
}
</style>