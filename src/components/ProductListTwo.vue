<template>
   <div id="product-list-two">
       <h2>Product List two</h2>
       <ul>
         <li v-for="product in products">
           <span class="name">{{ product.name }}</span>
           <span class="price">${{ product.price }}</span>
         </li>
       </ul>
   </div>
</template>

<script>
export default {
  computed:{
    products(){
      return this.$store.state.products;
    },
    saleProducts(){
       return this.$store.getters.saleProducts;
    }
  }

}
</script>

<style lang="css" scoped>
 #product-list-two{
   background: #d1e4ff;
   box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
 }
 #product-list-two ul{
   padding: 0;
   list-style-type:none;

 }

 #product-list-two li{
   margin-right: 10px;
   margin-top:10px;
   padding: 20px;
   background: rgba(255,255,255,0.7);
 }
 .price{
   font-weight: bold;
   color:#860ce8;
   display:block;
 }
</style>
