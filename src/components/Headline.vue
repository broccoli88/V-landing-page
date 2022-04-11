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
        </div>
        <Button>Roll in</Button>
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
    margin-bottom: 5rem;
}

.cta > h2 {
    background-color: var(--color-additional);
    width: fit-content;
    color: var(--color-secondary);
    margin-bottom: 3rem;
    text-transform: uppercase;
}

@media (min-width: 500px) {
    .hero {
        padding-top: 20rem;
    }

    .cta {
        width: 30em;
    }
}
</style>