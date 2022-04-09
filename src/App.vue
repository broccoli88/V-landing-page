<template>
    <NavBar />
    <Hero />
</template>

<script setup>
// IMPORTS
import NavBar from "./components/NavBar.vue";
import Hero from "./components/Hero.vue";
</script>



<style>
@import "./assets/base.css";

#app {
    width: 100vw;
    min-height: 100vh;
}
</style>
