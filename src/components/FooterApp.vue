<script>
import BlueFooter from './BlueFooter.vue'
import NavFooter from './NavFooter.vue'
import SigninFooter from './SigninFooter.vue'

export default {
    name: "FooterApp",
    components: {
        BlueFooter,
        NavFooter,
        SigninFooter
    }
}
</script>

<template>
    <BlueFooter />
    <NavFooter />
    <SigninFooter />
</template>

<style scoped></style>