<template>
  <div class="m-5">

    <div class="cards-container"> 
      <h3 class="text-left">Detalle del producto (modal)</h3>
      <div class="card d-flex flex-row text-white bg-dark" >
        <img class="card-img-top card-img" :src=this.detalle.imagen alt="Card image cap">
        <div class="d-flex flex-column p-5">
          <div class="card-body">
            <h2 class="card-title">{{ detalle.nombre }}</h2>
            <p class="card-text">En {{ detalle.lugar }}</p>
            <p class="card-text">Capacidad total {{ detalle.capacidad }} / {{ detalle.disponibilidad }} entradas disponibles</p>
          </div>
          <ul class="list-group list-group-flush text-dark">
            <li class="list-group-item">Fecha: {{ detalle.fecha }}</li>
            <li class="list-group-item">Apertura puertas: {{ detalle.apertura }}</li>
            <li class="list-group-item">Valor: £ {{ detalle.precio }}</li>
          </ul>
          <div class="card-body">
            <p>{{ detalle.descripcion }}</p>
            <a href="#" class="card-link btn btn-primary">Ver en mapa</a>
            <a href="#" class="card-link btn btn-warning">Comprar</a>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductDetail',
  props: {
    detalle: Object,

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.card-img{
  object-fit: cover; 
  width:800px;
}
</style>
