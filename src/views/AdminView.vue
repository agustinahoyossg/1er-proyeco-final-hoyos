<template>
   <div>
    <NavBarVue />
      <add-product/>
   </div>
</template>

<script>

import AddProduct from '@/components/AddProduct.vue'
import NavBarVue from '@/components/NavBar.vue';
export default {
  name: 'AdminView',
  components: {

    AddProduct,
    NavBarVue,
  }
}
</script>

<style scoped>

</style>