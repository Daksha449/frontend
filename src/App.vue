<template>
  <MyHeader Name="Grossy"/>
  <ProductBox :store=store  />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import ProductBox from  './components/ProductBox.vue'

export default {
  name: 'App',
  components: {
    // Step 2 register the component 
    MyHeader,
    ProductBox
  },

  data(){
    return {
      store: []
    }
  },
  methods: {
    // promises

      async fetchproducts(){
         const res= await fetch('https://abcde-lxpj.onrender.com/api')
         const data= await res.json()
         return data.document.store;
      }

  },

  async created(){

    this.store = await this.fetchproducts();
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
  background-color: honeydew;
  
}
.container {
  max-width: 40px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>
