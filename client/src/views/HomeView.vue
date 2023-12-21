<template>
    <div>
        <h1>HomeView.vue</h1>
    </div>
    <div class="products">
        <ProductCard v-for="item in products" :product="item" :key="item.id" />
    </div>
    <div class="">
        <h1 v-show="title">Главная</h1>
    </div>
    <input type="button" value="Click" @click="titleFunc">
</template>
<script>
import ProductCard from '../components/ProductCard.vue';



export default {
    components: {

        ProductCard: ProductCard,
    },
    data() {
        return {
            title: false,
        };
    },
    methods: {
        titleFunc(){
            this.title = !this.title;
        },
    },
};

</script>

<style scoped>
.products{
    display: flex;
    flex-wrap: wrap;

}
</style>