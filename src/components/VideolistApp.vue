<script>

export default {

    name: 'VideolistApp',
    data() {
        return {

        };
    },
};

</script>

<template>
    <div class="frame">

        <iframe width="840" height="550" src="https://www.youtube.com/embed/ZOEihZPz3aE" title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen></iframe>


        <div class="video-thumbs">

        </div>
    </div>
</template>

<style lang="scss" scoped>
.frame {
    margin-top: 50px;
    display: flex;
    flex-direction: row;

    .video-thumbs {
        height: 550px;
        width: calc(100% - 840px);
        background-color: blue;
    }
}
</style>