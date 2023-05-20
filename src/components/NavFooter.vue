<script>
export default {
    name: "NavFooter"
}
</script>

<template>
    <div id="container">
        <div id="contained">
            <nav>
                <!-- DC COMICS -->
                <div>
                    <h4>dc comics</h4>
                    <ul>
                        <li>Characters</li>
                        <li>Comics</li>
                        <li>Movies</li>
                        <li>TV</li>
                        <li>Games</li>
                        <li>Video</li>
                        <li>News</li>
                    </ul>
                </div>
                <!-- SHOP -->
                <div>
                    <h4>shop</h4>
                    <ul>
                        <li>Shop DC</li>
                        <li>Shop DC Collectables</li>
                    </ul>
                </div>
                <!-- DC -->
                <div>
                    <h4>dc</h4>
                    <ul>
                        <li>Terms of Use</li>
                        <li>Privacy policy (New)</li>
                        <li>Ad Choices</li>
                        <li>Advertising</li>
                        <li>Jobs</li>
                        <li>Subscription</li>
                        <li>Talent Workshop</li>
                        <li>CPSC Certificate</li>
                        <li>Rating</li>
                        <li>Shop Help</li>
                        <li>Contact Us</li>
                    </ul>
                </div>
                <!-- SITES -->
                <div>
                    <h4>sites</h4>
                    <ul>
                        <li>DC</li>
                        <li>MAD Magazine</li>
                        <li>DC Kids</li>
                        <li>DC Universe</li>
                        <li>DC Power Visa</li>
                    </ul>
                </div>
            </nav>
            <img src="../assets/dc-logo-bg.png">
        </div>
    </div>
</template>

<style scoped>
#container {
    width: 100%;
    height: 70vh;
    background-image: url(../assets/footer-bg.jpg);
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

nav {
    max-height: 100%;
    display: flex;
    flex-wrap: wrap;
    justify-content: start;
    align-items: start;
    flex-direction: column;
    padding: 3rem 0;
    gap: 1rem;
}

h4 {
    text-transform: uppercase;
}

ul {
    list-style: none;
    padding-bottom: 1rem;
}

img {
    overflow: hidden;
}
</style>