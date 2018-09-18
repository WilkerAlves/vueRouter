<template>
 <div class="details">
   <h1>{{title}}</h1>
   <h2>the product id is :{{this.$route.params.Pid}}</h2>
   <div class="col-md-12" v-for="(product,index) in products" :key="index">
     <div v-if="proId == product.productId">
      <h1>{{product.productTitle}}</h1>
      <img :src="product.image" class="img-fluid">
     </div>
    </div>
 </div>
</template>
<script>
export default {
  name: "details",
  data() {
    return {
      proId:this.$route.params.Pid,
      title: "details",
      products: [
        {
          productTitle: "ABCN",
          image: require("../assets/product1.png"),
          productId: 1
        },
        {
          productTitle: "KARMA",
          image: require("../assets/product2.png"),
          productId: 2
        },
        {
          productTitle: "Tino",
          image: require("../assets/product3.png"),
          productId: 3
        },
        {
          productTitle: "EFG",
          image: require("../assets/product4.png"),
          productId: 4
        },
        {
          productTitle: "MLI",
          image: require("../assets/product5.png"),
          productId: 5
        },
        {
          productTitle: "Banans",
          image: require("../assets/product6.png"),
          productId: 6
        }
      ]
    };
  }
};
</script>