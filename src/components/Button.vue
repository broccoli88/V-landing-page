<template>
    <button class="button">
        <slot></slot>
    </button>
</template>

<script>
</script>

<style>
.button {
    width: 10em;

    text-transform: uppercase;
    font-weight: 600;
    font-size: 1.8rem;
    font-family: var(--font-oswald);

    padding: 0.5em 1em;
    border: 0;

    display: flex;
    align-items: center;
    justify-content: center;

    cursor: pointer;
}

.button--style-headline {
    background-color: var(--color-additional);
    border: 2px solid var(--color-additional);
    color: var(--color-accent);
    font-family: var(--font-oswald);
}

.button:hover {
    filter: brightness(110%);
}
</style>