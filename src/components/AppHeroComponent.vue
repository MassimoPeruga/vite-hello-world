<script>
export default {
    name: 'Jumbo',
    data() {
        return {
            image: {
                name: 'jumbo.jpg',
                alt: 'Jumbo',
            },
        };
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    },
};
</script>

<template>
    <img :src="getImagePath(`../assets/img/${image.name}`)" :alt="image.alt">
</template>

<style scoped>
img {
    height: 75%;
    border-radius: 20px;
}
</style>