<template>
    <div class="promotion">
        <div class="promo-description">
            <h3>Sign Up for our Newsletter!</h3>
            <h2>Get Informed first about our promotions!</h2>
            <p>
                Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Quibusdam quo aut, consequuntur similique hic distinctio.
            </p>
            <Button class="newsletter-button">Sign Up </Button>
        </div>
        <div class="newsletter-img">
            <img src="../assets/Newsletter.png" alt="" />
        </div>
    </div>
</template>

<script>
import Button from "../reusable/Button.vue";

export default {
    components: { Button },
};
</script>

<style>
.promotion {
    width: 100%;
    padding-inline: var(--padding-inline);
    padding-block: 30% 40%;

    position: relative;
}

.promotion::after {
    content: "";
    display: inline-block;

    background-color: var(--color-bg);
    clip-path: polygon(0 100%, 100% 0, 100% 100%, 0% 100%);

    width: 100%;
    height: 15rem;
    position: absolute;
    top: -15rem;
    left: 0;

    /* z-index: -10; */
}

.promo-description {
    width: fit-content;
    display: flex;
    flex-direction: column;
}

.promo-description > h2 {
    font-family: var(--font-lobster);
    /* font-size: 3rem; */
    color: var(--color-accent);
    margin-bottom: 3rem;
}

.promo-description > h3 {
    font-family: var(--font-oswald);
    background: var(--color-additional);
    width: fit-content;
    padding: 0 0.5em;
}

.promo-description > p {
    margin: 0;
    width: min(90%, 25em);
    word-wrap: break-word;
    word-break: break-all;
    margin-bottom: 6rem;
}

.newsletter-button {
    background-color: var(--color-additional);
}

.newsletter-img {
    display: none;
}

@media (min-width: 768px) {
    .promotion {
        padding-block: 5%;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 4rem;
    }

    .promo-description {
        width: min(90%, 30em);
    }

    .promo-description > p {
        flex: 1.5;
    }

    .newsletter-img {
        display: inline;
        flex: 2;
        max-width: 500px;
    }

    .newsletter-img > img {
        width: 100%;
        object-fit: cover;
    }

    .promo-description > p {
        flex: 1.5;
    }
}
</style>