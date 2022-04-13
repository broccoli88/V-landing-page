<template>
    <div class="sub-headline">
        <div class="sub__description">
            <h3>Comfortable and cheap flights</h3>
            <h2>Fly in an affordable way</h2>
            <p>
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quae
                sapiente, doloribus dicta eveniet, possimus consequuntur
                voluptatem u
            </p>
            <Button class="btn--style-sub-headline"> Check </Button>
        </div>
        <div class="img-container">
            <img src="../assets/wallet.jpg" alt="" />
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
.sub-headline {
    width: 100%;
    background-color: var(--color-additional);
    padding-inline: var(--padding-inline);
    padding-block: 15%;

    display: flex;
}

.sub__description {
    width: fit-content;
    /* padding-inline: var(--padding-inline); */

    display: flex;
    flex-direction: column;
}

.sub__description > h2 {
    font-family: var(--font-lobster);

    font-size: clamp(3rem, 5vw, 6rem);
    color: var(--color-accent);
    margin-bottom: 3rem;
}

.sub__description > h3 {
    /* margin-top: 30%; */
    font-family: var(--font-oswald);
    text-transform: uppercase;
    background-color: white;
    width: fit-content;
    color: var(--color-additional);
}

.sub__description > p {
    margin: 0;
    width: min(90%, 25em);
    word-wrap: break-word;
    word-break: break-all;

    margin-bottom: 6rem;
}

.btn--style-sub-headline {
    background-color: white;
    color: var(--color-accent);
}

.img-container {
    display: none;
}

.btn--style-sub-headline:hover {
    filter: brightness(98%);
}

@media (min-width: 768px) {
    .sub-headline {
        align-items: center;
        gap: 4rem;
        justify-content: center;
        padding-block: 10%;
    }

    .sub__description {
        width: fit-content;
        flex: 1.5;
    }

    .img-container {
        display: inline-block;
        max-height: 20em;
        flex: 2;
        position: relative;
        display: flex;
        align-items: center;
    }

    .img-container::before {
        content: "";
        display: inline-block;
        width: 110%;
        height: 110%;
        border: 10px solid hsl(0, 0%, 100%);

        position: absolute;
        top: -5%;
        left: -5%;
    }

    .img-container > img {
        width: 100%;
        height: 20em;
        object-fit: cover;
    }
}
</style>