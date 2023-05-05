<template>
   
    <div class="grid">
        <div class="" v-for="product of store" :key="product.id" >
            <SingleProduct :product=product />
        </div>
    </div>

</template>
<script>
import SingleProduct from './SingleProduct.vue'

export default {
    name: 'ProductBox',
    props:{
        store: Array
    },
    components:{
        SingleProduct
    }
    
}
</script>
<style scoped>
.grid{
    display: grid;
    grid-template-columns:1fr 1fr 1fr;
    gap: 30px;
}
</style>
