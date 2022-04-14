<template>
    <div class="offers">
        <h2 class="header">Check our best offers!</h2>
        <Icon
            v-if="!allPromos"
            @click="slideRight"
            class="slide right"
            icon="bi:chevron-double-left"
            color="black"
            width="24"
            height="24"
            :rotate="2"
            :inline="true"
        />

        <component v-if="!allPromos" :is="activeComponent"></component>
        <div v-if="allPromos" class="promos">
            <CardOne />
            <CardThree class="best" />
            <CardTwo />
        </div>

        <Icon
            v-if="!allPromos"
            @click="slideLeft"
            class="slide left"
            icon="bi:chevron-double-left"
            color="black"
            width="24"
            height="24"
            :rotate="4"
            :inline="true"
        />
    </div>
</template>

<script>
import CardOne from "./CardOne.vue";
import CardThree from "./CardThree.vue";
import CardTwo from "./CardTwo.vue";

import { Icon } from "@iconify/vue";
export default {
    components: { CardOne, CardTwo, CardThree, Icon },

    data() {
        return {
            promoList: ["CardOne", "CardTwo", "CardThree"],
            activeComponent: "CardThree",
            allPromos: true,
        };
    },

    mounted() {
        window.addEventListener("resize", this.checkWidth);
        this.checkWidth();
    },

    methods: {
        slideRight() {
            if (this.activeComponent === "CardOne") {
                this.activeComponent = "CardTwo";
            } else if (this.activeComponent === "CardTwo") {
                this.activeComponent = "CardThree";
            } else if (this.activeComponent === "CardThree") {
                this.activeComponent = "CardOne";
            }
        },

        slideLeft() {
            if (this.activeComponent === "CardOne") {
                this.activeComponent = "CardThree";
            } else if (this.activeComponent === "CardThree") {
                this.activeComponent = "CardTwo";
            } else if (this.activeComponent === "CardTwo") {
                this.activeComponent = "CardOne";
            }
        },

        checkWidth() {
            const width = window.innerWidth;

            if (width >= 900) {
                this.allPromos = true;
            } else {
                this.allPromos = false;
            }
        },
    },
};
</script>

<style>
.offers {
    padding-inline: var(--padding-inline);
    padding-block: 8rem;
    width: 100%;
    position: relative;
}

.header {
    font-family: var(--font-lobster);
    color: var(--color-accent);
    text-align: center;
    margin-bottom: 6rem;
}

.slide {
    cursor: pointer;

    position: absolute;
    top: 50%;

    transform: translateY(-50%);
}

.left {
    left: 1rem;
}

.right {
    right: 1rem;
}

@media (min-width: 900px) {
    .promos {
        display: flex;
        gap: 3rem;
        justify-content: center;
    }

    .promos:nth-child(1) {
        align-self: flex-end;
    }

    .best {
        transform: scale(1.1);
    }
}
</style>