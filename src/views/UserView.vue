<template>
   <div>
    <NavBarVue/>
      <product-list/>
      <cart :misProductos=this.productosCart />
      <ProductDetail :detalle="this.productosCart[0]"/>
   </div>
</template>

<script>
import ProductList from '@/components/ProductList.vue'
import NavBarVue from '@/components/NavBar.vue';
import Cart from '@/components/Cart.vue'
import ProductDetail from '@/components/ProductDetail.vue';

export default {
  name: 'UserView',
  components: {
    ProductList,
    Cart,
    NavBarVue,
    ProductDetail
},
  data() {
    return {
      productosCart: [{nombre:"Metallica", eventplace:"Samsung Arena",capacity:20000, description:"Los lengendarios del trash metal vuelven con un show unico",doorsopenat:"20:00 HS",availabletikets:1220, fecha:"22/05/2023", precio: 155}, {nombre:"evento 5", fecha:"02/01/2023", precio: 15}
      ]
    }
  }
}
</script>

<style scoped>

</style>