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
    <div id="container">
        <div id="contained">
            <div v-for="content in menu" class="card">
                <img :src="getImagePath(`${content.cardImg}`)">
                <p>{{ content.text.toUpperCase() }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
#container {
    width: 100%;
    height: 20vh;
    background-color: #0282f9;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
}

#contained {
    width: 70%;
    height: 100%;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
}

.card {
    display: flex;
    align-items: center;
}

img {
    max-height: 50px;
    max-width: 50px;
    margin-right: 1rem;
}

p {
    white-space: nowrap;
}
</style>