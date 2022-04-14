<template>
    <Promo>
        <h3 class="destination">Norway</h3>
        <p class="promo-hook">You must check Norway landscape!</p>
        <p class="price">1500$</p>
        <div class="card2-img"></div>
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
.card2-img {
    width: 100%;
    height: 10rem;
    background-image: url("../assets/norway.jpg");
    background-size: cover;
    background-position: center;
}
</style>