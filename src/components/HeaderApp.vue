<script>
export default {
    name: "HeaderApp",
    data() {
        return {
            menu: ["characters", "comics", "movies", "tv", "games", "collectionables", "video", "fans", "news", "shop"]
        }
    },
    methods: {

    }
}
</script>

<template>
    <div id="container">
        <img src="../assets/dc-logo.png" alt="Logo">

        <div id="menuContainer">
            <div v-for="components in menu" class="menuCell">
                <a href="#" :class="(components == 'comics') ? 'selected' : ''">{{ components.toUpperCase() }}</a>
                <div v-if="components == 'comics'" id="current"></div>
            </div>
        </div>
    </div>
</template>

<style scoped>
#container {
    width: 70%;
    height: 20vh;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

#menuContainer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 70%;
    height: 100%;
}

.selected {
    color: #0282f9;
}

.menuCell {
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: relative;
}

a {
    color: black;
    text-decoration: none;
}

#current {
    width: 50%;
    height: 5%;
    background-color: #0282f9;
    position: absolute;
    bottom: 0%;
    transform: translate(-50%, 0px);
    left: 50%;

}
</style>