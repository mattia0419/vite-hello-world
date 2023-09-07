<script>
export default {
    data() {
        return {
            image: "mine.jpg",
        }
    },

    methods: {
        buildingImagePath() {
            const imageURL = new URL('../assets/img/' + this.image, import.meta.url);
            console.log(imageURL);

            return imageURL.href;
        }
    }
}
</script>


<template>
    <img :src="buildingImagePath()" alt="">
</template>