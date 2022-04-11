<template>
    <button class="button button--style">
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

    padding: 0.5em 1em;
    border: 0;

    display: flex;
    align-items: center;
    justify-content: center;
}

.button--style {
    background-color: var(--color-additional);
    border: 2px solid var(--color-additional);
    color: var(--color-accent);
    font-family: var(--font-oswald);
}

.button:hover {
    filter: brightness(105%);
}
</style>