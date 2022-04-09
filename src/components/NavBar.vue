<template>
    <div class="nav-container">
        <span class="logo">Traveler</span>
        <div class="burger" @click="toggleNav" v-if="showBurger">
            <div class="line" :class="{ line1: showNavMobile }"></div>
            <div class="line" :class="{ line2: showNavMobile }"></div>
            <div class="line" :class="{ line3: showNavMobile }"></div>
        </div>

        <nav>
            <transition @enter="onEnter" name="nav-slide">
                <ul class="nav-links-mobile" v-if="showNavMobile">
                    <li>Offer</li>
                    <li>Destinations</li>
                    <li>Prices</li>
                    <li>About</li>
                    <li>Contact</li>
                </ul>
            </transition>
        </nav>

        <nav v-if="showNavBar" class="standard-nav">
            <ul class="nav-links">
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
import gsap from "gsap";
export default {
    data() {
        return {
            showNavMobile: null,
            showNavBar: null,
            showBurger: null,
        };
    },

    mounted() {
        window.addEventListener("resize", this.checkWidth);
        this.checkWidth();
    },

    methods: {
        toggleNav() {
            this.showNavMobile = !this.showNavMobile;
        },

        onEnter(el) {
            const links = el.children;
            gsap.to(links, {
                x: 0,
                opacity: 1,
                stagger: {
                    amount: 0.2,
                },
            });
        },

        checkWidth() {
            const check = window.innerWidth;

            if (check >= 650) {
                this.showBurger = false;
                this.showNavMobile = false;
                this.showNavBar = true;
            } else {
                this.showBurger = true;
                this.showNavBar = false;
            }
        },
    },
};
</script>

<style>
.nav-container {
    height: 7rem;

    display: flex;
    align-items: center;
    justify-content: space-between;

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
    color: var(--color-secondary);

    position: relative;

    transform: translateX(420px);
    opacity: 0;

    transition: all 0.3s ease;
}

.nav-links-mobile > li::before {
    content: "";
    display: inline-block;
    width: 100%;
    height: 2px;
    background-color: hsla(0, 15%, 52%, 0.5);
    box-shadow: 0 2px 2px hsla(0, 15%, 52%, 0.5);

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

.nav-slide-enter-from,
.nav-slide-leave-to {
    transform: translateX(250px);
    opacity: 0;
}

.nav-slide-enter-active,
.nav-slide-leave-active {
    transition: all 0.5s ease;
}

.standard-nav {
    width: 95%;

    position: fixed;
    /* top: 0;
    left: 0; */
}

.nav-links {
    width: 100%;
    list-style: none;
    font-family: var(--font-lobster);

    display: flex;
    justify-content: flex-end;
    gap: 0.3em;
}

.nav-links > li {
    cursor: pointer;
    width: 6em;
    text-align: center;
    color: var(--color-secondary);

    position: relative;
}

.nav-links > li:hover {
    font-weight: 700;
}

@media (min-width: 650px) {
}
</style>