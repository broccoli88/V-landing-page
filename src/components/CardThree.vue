<template>
    <Promo>
        <div class="best-price">Best Price</div>
        <h3 class="destination">Japan</h3>
        <p class="promo-hook">- Something you have never seen -</p>
        <p class="price">1200$</p>
        <div class="card3-img"></div>
        <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit.
            Consequuntur ad reiciendis necessitatibus repellendus, quas culpa
            voluptatibus. Quisquam facilis hic aut.
        </p>
    </Promo>
</template>

<script>
import Promo from "../reusable/Promo.vue";
export default {
    components: { Promo },
};
</script>

<style>
.card3-img {
    width: 100%;
    height: 10rem;
    background-image: url("../assets/japan.jpg");
    background-size: cover;
    background-position: center;
}

.best-price {
    width: 100%;
    height: 3rem;
    background-color: var(--color-additional);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 2rem;
    color: var(--color-secondary);
}
</style>