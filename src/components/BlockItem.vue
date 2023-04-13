<script>

export default {

    name: 'BlockItem',
    data() {
        return {};
    },

    props: {
        block: Object,
    }
};

</script>

<template>
    <div class="block">
        <ul>
            <strong>{{ block.title }}</strong>
            <li v-for="link in block.links">{{ link }}</li>
        </ul>
    </div>
</template>

<style lang="scss" scoped></style>