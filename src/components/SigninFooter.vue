<script>
export default {
    name: "SigninFooter",
    data() {
        return {
            links: ["../assets/footer-facebook.png", "../assets/footer-twitter.png", "../assets/footer-youtube.png", "../assets/footer-pinterest.png", "../assets/footer-periscope.png"]
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
            <button>sign-up now!</button>
            <div id="follow">
                <h3>follow us</h3>
                <a v-for="link in links" href="#"><img :src="getImagePath(`${link}`)"></a>
            </div>
        </div>
    </div>
</template>

<style scoped>
#container {
    width: 100%;
    height: 20vh;
    background-color: #303030;
    background-repeat: no-repeat;
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
}

#contained {
    width: 70%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

button {
    border: 3px solid #0282f9;
    padding: 1rem;
    background-color: #303030;
    color: white;
    text-transform: uppercase;
}

#follow {
    width: 35%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    text-transform: uppercase;
    color: #0282f9;
}

h3 {
    font-size: 20px;
}
</style>