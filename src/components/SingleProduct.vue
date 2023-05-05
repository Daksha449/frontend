<template>
    

    <div  :class="product.In_stock ? 'black': 'white' ">
                        <h1>{{product.productname}}</h1>
                        <h2> Price : {{product.price}}</h2>
                        <h3>Stock Available : {{product.stock_available}}</h3>
                        <h4>Exp_date : {{ product.Exp_date }}</h4>
                        
    </div>
</template>

<script>

export default{
    name: 'SingleProduct',
    props:{
        product: Array
    }
}
</script>

<style scoped>

.black{
   background-color: #bbf7d0;
}

h4{
    margin: 2px;
}

div{
    background-color: #ffb89e;
    color: black;
    padding: 3em;
    text-align: center;
    width: 80%;
    margin: auto;
    border-radius: 7px;
    

}

.white{
background-color:#fca5a5 !important;

}


</style>