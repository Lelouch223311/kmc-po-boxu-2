<template>
    <div>
        <h1>HomeView.vue</h1>
    </div>
    <div class="products">
        <ProductCard v-for="item in products" :product="item" :key="item.id" />
    </div>
</template>
<script>
import ProductCard from '../components/ProductCard.vue';



export default {
    components: {

        ProductCard: ProductCard,
    },
    data() {
        return {};
    },
    methods: {},
};

</script>

<style scoped>
.products{
    display: flex;
    flex-wrap: wrap;

}
</style>