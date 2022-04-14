<template>
    <Promo>
        <h3 class="destination">Arizona</h3>
        <p class="promo-hook">Want to ride Route no. 66?</p>
        <p class="price">1200$</p>
        <div class="card1-img"></div>
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
.card1-img {
    width: 100%;
    height: 10rem;
    background-image: url("../assets/Arizona1.jpg");
    background-size: cover;
    background-position: center;
}
</style>