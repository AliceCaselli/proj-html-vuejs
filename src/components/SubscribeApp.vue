<script>

export default {

    name: 'SubscribeApp',
    data() {
        return {};
    },
};

</script>

<template>
    <div class="subscribe">

        <strong>SUBSCRIBE TO NEWSLETTER</strong>
        <input type="text" placeholder="Email">
        <button>SUBSCRIBE</button>
    </div>
</template>

<style lang="scss" scoped>
.subscribe {
    display: flex;
    flex-direction: column;
    gap: 10px;

    strong {
        padding-bottom: 5px;
    }

    input {
        background-color: #fff;
        border-color: transparent;
        padding: 10px;
        border-radius: 5px;
    }

    button {
        background-color: #545454;
        border-color: transparent;
        border-radius: 5px;
        font-size: .7em;
        padding: 10px;
    }
}
</style>