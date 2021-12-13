<template>
    <div id="app">
        <FixedIcons />

        <!-- <ScrollWidget /> -->

        <Header id="header"/>

        <Jumbo />

        <Main />

        <Footer />

        <Copyright />
    </div>
</template>

<script>
import FixedIcons from "./components/FixedIcons.vue";
// import ScrollWidget from "./components/ScrollWidget.vue"
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";
import Jumbo from "./components/Jumbo.vue";
import Copyright from "./components/Copyright.vue";

export default {
    name: "App",
    components: {
        // ScrollWidget,
        FixedIcons,
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
