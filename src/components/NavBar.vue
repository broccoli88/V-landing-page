<template>
    <div class="nav-bar-mobile">
        <span class="logo">Traveler</span>
        <div class="burger" @click="toggleNav">
            <div class="line" :class="{ line1: showNavMobile }"></div>
            <div class="line" :class="{ line2: showNavMobile }"></div>
            <div class="line" :class="{ line3: showNavMobile }"></div>
        </div>
        <nav>
            <ul class="nav-links-mobile" v-show="showNavMobile">
                <li>Offer</li>
                <li>Destinations</li>
                <li>Prices</li>
                <li>About</li>
                <li>Contact</li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showNavMobile: false,
        };
    },

    methods: {
        toggleNav() {
            const links = document.querySelectorAll(".nav-links-mobile li");
            this.showNavMobile = !this.showNavMobile;
            console.log(links);
        },
    },
};
</script>

<style>
.nav-bar-mobile {
    height: 7rem;

    display: flex;
    align-items: center;

    box-shadow: 0 0 10px hsl(0, 0%, 0%, 0.5);

    padding: 0.5em 2em;
    position: relative;
    background-color: var(--color-additional);
}

.logo {
    font-family: var(--font-lobster);
    font-size: 2.5rem;
}

.burger {
    width: 25px;
    height: 25px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;

    cursor: pointer;

    position: fixed;
    top: 2rem;
    right: 3rem;

    z-index: 9999;
}

.line {
    width: 100%;
    height: 3px;
    background-color: black;
    transition: all 0.3s ease;
}

.nav-links-mobile {
    width: 60%;
    max-width: 250px;
    height: 100vh;
    background-color: var(--color-additional);

    font-family: var(--font-lobster);
    font-size: 2rem;

    padding: 1em 0 0 5rem;
    list-style: none;

    box-shadow: 0 7rem 10px hsl(0, 0%, 0%, 0.5);

    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 4rem;

    position: fixed;
    top: 0;
    right: 0;
}

.nav-links-mobile > li {
    width: 100%;

    position: relative;
    transition: all 0.3s ease;
}

.nav-links-mobile > li::before {
    content: "";
    display: inline-block;
    width: 100%;
    height: 2px;
    background-color: hsl(0, 0%, 0%, 0.5);
    box-shadow: 0 2px 2px hsl(0, 0%, 0%, 0.5);

    position: absolute;
    bottom: 0;
    left: 0;

    transform: translateX(100%);
    opacity: 0;
    transition: all 0.3s ease;
}

.nav-links-mobile > li:hover {
    font-weight: bold;
}

.nav-links-mobile > li:hover::before {
    transform: translateX(0);
    opacity: 1;
}

.line1 {
    transform: rotateZ(-45deg) translateY(5px) translateX(-6px);
}

.line2 {
    transform: rotateZ(45deg) translateY(-0px);
}

.line3 {
    transform: translateY(10px);
    opacity: 0;
}
</style>