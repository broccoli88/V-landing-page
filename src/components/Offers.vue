<template>
    <div class="offers">
        <Icon
            class="slide right"
            icon="bi:chevron-double-left"
            color="black"
            width="24"
            height="24"
            :rotate="2"
            :inline="true"
        />
        <CardOne />
        <Icon
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
import { Icon } from "@iconify/vue";
export default {
    components: { CardOne, Icon },
};
</script>

<style>
.offers {
    padding: var(--padding-inline);
    width: 100%;
    position: relative;
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
</style>