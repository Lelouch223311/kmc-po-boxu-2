<template>
    <div>
        <h1>HomeView.vue</h1>
    </div>



    <div class="">
        <h1 v-show="title">Главная</h1>
    </div>
</template>
<script>
import ProductCard from '../components/ProductCard.vue';



export default {

    data() {
        return {
            products: [],
            title: false,
            inputValue: null,

        };
    },
    methods: {
        titleFunc(event) {
            this.title = !this.title;
        },

        // myFunc(event){
        //     alert('Alert Bro')
        // },
    },
};

</script>

<style scoped>
.products {
    display: flex;
    flex-wrap: wrap;

}
</style>