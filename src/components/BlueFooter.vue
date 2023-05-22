<script>
export default {
    name: "BlueFooter",
    data() {
        return {
            menu: [
                {
                    cardImg: "../assets/buy-comics-digital-comics.png",
                    text: "digital comics"
                },
                {
                    cardImg: "../assets/buy-comics-merchandise.png",
                    text: "dc merchandise"
                },
                {
                    cardImg: "../assets/buy-comics-shop-locator.png",
                    text: "comic shop locato"
                },
                {
                    cardImg: "../assets/buy-comics-subscriptions.png",
                    text: "subscription"
                },
                {
                    cardImg: "../assets/buy-dc-power-visa.svg",
                    text: "dc power visa"
                }
            ]
        }
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="width-100per std-height bg-blue flex jc-center ai-center">
        <div class="std-width height-100per flex jc-evenly ai-center">
            <div v-for="content in menu" class="card">
                <div class="blueFooterImg">
                    <img :src="getImagePath(`${content.cardImg}`)">
                </div>
                <p>{{ content.text.toUpperCase() }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    align-items: center;
}

.blueFooterImg {
    height: 50px;
    width: 50px;
    margin-right: 1rem;
}

img {
    max-width: 100%;
    max-height: 100%;
}

p {
    white-space: nowrap;
}
</style>