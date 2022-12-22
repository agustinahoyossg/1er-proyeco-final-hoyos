<template>
  <div class="cards-wrapper">
    <ProductCard  v-for="(evento, index) of this.eventos" :key="index" :detalle="evento" :evento="evento.name" :precio="+evento.price" :imagen="evento.image" :fecha="evento.date" :lugar="evento.eventplace"   :descripcion="evento.description" :puertas="evento.doorsopenat" :localidades=+evento.availabletickets :capacidadtotal=+evento.capacity :id=+evento.id  />
  </div>
</template>

<script>
import axios from 'axios'
import ProductCard from './ProductCard.vue';

export default {
  name: 'ProductList',
  components: {
    ProductCard
  },
  props: {
    productos: Array
  },
  data() {
    return {
      eventos: []
    }
  },
  created(){
    const URLGET = "https://63a21bbcba35b96522f039e2.mockapi.io/londonevents/events"
            axios.get(URLGET)
            .then((response) => {
              this.eventos = response.data
            })
           .catch((err) => {console.error(`${err}`)})
        },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.cards-wrapper {
  display: flex;
  flex-wrap: wrap;
}
</style>


