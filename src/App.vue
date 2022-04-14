<template>
    <!-- <NavBar /> -->
    <Headline />
    <main>
        <Offers />
        <SubHeadline />
        <Promotion />
        <Connections />
    </main>
</template>

<script>
// IMPORTS
import NavBar from "./components/NavBar.vue";
import Headline from "./components/Headline.vue";
import Offers from "./components/Offers.vue";
import SubHeadline from "./components/SubHeadline.vue";
import Promotion from "./components/Promotion.vue";
import Connections from "./components/Connections.vue";

export default {
    components: {
        NavBar,
        Headline,
        SubHeadline,
        Offers,
        Promotion,
        Connections,
    },
};
</script>



<style>
@import "./assets/base.css";

#app {
    width: 100vw;
    min-height: 100vh;
}
</style>
