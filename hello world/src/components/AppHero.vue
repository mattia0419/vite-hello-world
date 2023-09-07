<script>
export default {
    data() {
        return {
            image: "mine.jpg",
        }
    },

    methods: {
        buildingImagePath(imageName) {
            const imageURL = new URL('../assets/img/' + imageName, import.meta.url);
            console.log(imageURL);

            return imageURL.href;
        }
    }
}
</script>


<template>
    <img :src="buildingImagePath(image)" alt="">
</template>