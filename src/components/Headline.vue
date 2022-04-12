<template>
    <div class="hero">
        <div class="cta">
            <h1>Want to fly?</h1>
            <h2>You will get where you want!</h2>
            <p>
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. Labore
                nemo non debitis sit quas vel dignissimos expedita officiis
                asperiores ut error, vitae nesciunt odio temporibus quisquam
                itaque deleniti sequi animi?
            </p>
            <Button class="button--style-headline">Roll in</Button>
        </div>
    </div>
</template>

<script>
import Button from "./Button.vue";

export default {
    components: { Button },
    data() {
        return {};
    },
};
</script>

<style>
.hero {
    width: 100%;
    height: 100vh;

    padding-top: 40%;
    padding-inline: 2rem;

    background-image: url("../assets/airplane.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;

    display: flex;
    flex-direction: column;
}

.cta {
    width: fit-content;
    margin-bottom: 5rem;

    display: flex;
    flex-direction: column;
}

.cta > h2 {
    background-color: var(--color-additional);
    width: fit-content;
    color: var(--color-secondary);
    text-transform: uppercase;
    z-index: 0;
    padding: 0.2em;
}

.cta > p {
    width: min(100%, 30em);
    word-wrap: break-word;
    word-break: break-all;

    margin: 4rem 0 6rem;
}

@media (min-width: 500px) {
    .hero {
        padding-top: 20rem;
    }
}

@media (min-width: 600px) {
    .hero {
        align-items: center;
    }

    .cta {
        width: min(80%, 35em);
        background-color: hsl(0, 0%, 100%, 0.5);
        align-items: center;

        padding: 3rem;

        position: relative;
    }

    .cta::before {
        content: "";
        display: inline-block;
        width: 110%;
        height: 110%;
        border: 10px solid hsl(0, 0%, 100%, 0.5);

        position: absolute;
        top: -5%;
        left: -5%;
    }
}
</style>