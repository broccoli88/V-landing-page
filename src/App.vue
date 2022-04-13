<template>
    <!-- <NavBar /> -->
    <Headline />
    <main>
        <Offers />
        <SubHeadline />
    </main>
</template>

<script>
// IMPORTS
import NavBar from "./components/NavBar.vue";
import Headline from "./components/Headline.vue";
import Offers from "./components/Offers.vue";
import SubHeadline from "./components/SubHeadline.vue";

export default {
    components: { NavBar, Headline, SubHeadline, Offers },
};
</script>



<style>
@import "./assets/base.css";

#app {
    width: 100vw;
    min-height: 100vh;
}
</style>
