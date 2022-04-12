<template>
    <!-- <NavBar /> -->
    <Headline />
    <main>
        <SubHeadline />
    </main>
</template>

<script>
// IMPORTS
import NavBar from "./components/NavBar.vue";
import Headline from "./components/Headline.vue";

import SubHeadline from "./components/SubHeadline.vue";

export default {
    components: { NavBar, Headline, SubHeadline },
};
</script>



<style>
@import "./assets/base.css";

#app {
    width: 100vw;
    min-height: 100vh;
}
</style>
