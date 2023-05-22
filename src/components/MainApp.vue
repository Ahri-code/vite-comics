<script>

export default {
    name: "MainApp",
    props: {
        comic: [
            {
                link: Array,
                cost: Array,
                series: Array,
                type: Array
            }
        ]
    },
    data() {
        return {

        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
// console.log(link);

</script>

<template>
    <div class="std-width flex ai-center">
        <div v-for="elements in comic">
            <img :src="getImagePath(`${elements.link}`)">
        </div>
    </div>
</template>

<style scoped></style>