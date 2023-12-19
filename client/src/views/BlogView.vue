<template>


    <div class="products">
        <ProductCard v-for="item in products" :product="item" :key="item.id" />
    </div>
 
</template>

<script>
import ProductCard from '../components/ProductCard.vue';
export default {
   components:{
       ProductCard: ProductCard
   },
   data () {
       return{
           products: [],
       }
   },
   methods: {

   },
   async beforeMount(){
       const data = await fetch('http://localhost:1337/api/products?populate=*')
       const js = await data.json()
       this.products = js.data
   }
   }

</script>

<style scoped>
.products{
    width: 95%;
    margin: 40px auto;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
}

</style>