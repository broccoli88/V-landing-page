<template>
    <div class="sub-headline">
        <div class="sub__description">
            <h3>Comfortable and cheap flights</h3>
            <h2>Fly in an affordable way</h2>
            <p>
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quae
                sapiente, doloribus dicta eveniet, possimus consequuntur
                voluptatem ut illum autem saepe alias veritatis provident
                suscipit dolores inventore nam. Voluptas, voluptates vel!
            </p>
            <Button class="btn--style-sub-headline"> Check </Button>
        </div>
    </div>
</template>

<script>
import Button from "./Button.vue";

export default {
    components: { Button },
};
</script>

<style>
.sub-headline {
    width: 100vw;
    background-color: var(--color-additional);

    display: flex;
    align-items: center;
}

.sub__description {
    padding-inline: 2rem;
    display: flex;
    flex-direction: column;
}

.sub__description > h2 {
    font-family: var(--font-lobster);
    font-size: 3rem;
    color: var(--color-accent);
    margin-bottom: 3rem;
}

.sub__description > h3 {
    margin-top: 30%;
    font-family: var(--font-oswald);
    text-transform: uppercase;
    background-color: white;
    width: fit-content;
    color: var(--color-additional);
}

.sub__description > p {
    margin: 0;
    width: min(100%, 30em);
    word-wrap: break-word;
    word-break: break-all;

    margin-bottom: 6rem;
}

.btn--style-sub-headline {
    background-color: white;
    color: var(--color-accent);

    margin-bottom: 6rem;
}

.btn--style-sub-headline:hover {
    filter: brightness(98%);
}
</style>