<template>
    <div class="promo-card">
        <slot> </slot>
        <Button class="btn-promo"> Get on Board</Button>
    </div>
</template>

<script>
import Button from "../reusable/Button.vue";
export default {
    components: { Button },
};
</script>

<style>
.promo-card {
    width: min(100%, 400px);
    padding: 2rem;
    margin-inline: auto;
    font-size: clamp(1.2rem, 1.5vw, 1.7rem);

    border: 1px solid var(--color-secondary);
    box-shadow: 0 0 10px hsl(0, 0%, 40%, 0.5);

    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5em;
}

.promo-card > h3 {
    font-size: 2.5rem;
}

.promo-card p {
    text-align: center;
}

.promo-hook {
    text-transform: uppercase;
    font-size: 95%;
    color: var(--color-secondary);
}

.price {
    font-size: 5rem;
    color: var(--color-primary);
    font-weight: bold;
    text-shadow: 0 0 1px hsl(0, 0%, 0%, 0.5);
}

.btn-promo {
    margin-top: 2rem;
    border: 1px solid var(--color-secondary);
    color: var(--color-secondary);
    background-color: transparent;
}

@media (min-width: 900px) {
    .promo-card {
        margin: 0;
    }
}
</style>