<script>

import BlockItem from './BlockItem.vue';
import SubscribeApp from './SubscribeApp.vue';

export default {

    name: 'UpfooterApp',
    data() {
        return {
            blocks: [
                {
                    title: 'GET STARTED',
                    links: [
                        'Resources',
                        'Tutorials',
                        'Examples',
                        'Docs',
                    ],
                },
                {
                    title: 'ABOUT',
                    links: [
                        'Stories',
                        'Community',
                        'Blog',
                        'Brand Assets',
                    ],
                },
                {
                    title: 'FEATURES',
                    links: [
                        'Overview',
                        'Design',
                        'Code',
                        'Collaborate',
                    ],
                },
                {
                    title: 'QUICK LINKS',
                    links: [
                        'Stories',
                        'Community',
                        'Blog',
                        'Brand Assets',
                    ],
                },
            ],
        };
    },

    components: {
        BlockItem,
        SubscribeApp,
    }
};

</script>

<template>
    <div class="up-footer">

        <BlockItem v-for="block in blocks" :block="block"></BlockItem>
        <SubscribeApp></SubscribeApp>
    </div>
</template>

<style lang="scss" scoped>
.up-footer {
    padding: 60px 0;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    border-bottom: 2px solid #f3f3f369;
}
</style>