<template>
    <div id="app">
        <Header />

        <Jumbo />

        <Main />

        <Footer />

        <Copyright />
    </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import Jumbo from "./components/Jumbo.vue";
import Copyright from "./components/Copyright.vue"

export default {
    name: "App",
    components: {
        Header,
        Main,
        Footer,
        Jumbo,
        Copyright,
    },
};
</script>

<style lang="scss">

</style>
