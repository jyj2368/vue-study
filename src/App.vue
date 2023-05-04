<template>
  <div>
    <div class="menu">
      <a v-for="(menu,index) in menu" :key="index">{{ menu }}</a>
    </div>

    <div v-for="(products,index) in products" :key="index" class="product">
      <h4>{{ products.location }}</h4>
      <p>{{ products.price }}</p>
    </div>

  </div>
</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      menu:['Home','Shop','About'],
      products:[{location : '역삼동 원룸', price : '80만원'},{location : '논현동 원룸', price : '70만원'},{location : '계산동 원룸', price : '40만원'}]
    }
  },
  components: { 

  }
}
</script>

<style>
  #app{
    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
    color:  #2c3e50;
  }
  .menu{
    background-color: darkslateblue ;
    padding: 15px;
    border-radius: 5px;
  }
  .menu a{
    color: #FFF;
    padding: 10px;
  }
</style>