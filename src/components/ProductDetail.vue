<template>
  <div class="m-5">

    <div class="cards-container"> 
      <h3 class="text-left">Detalle del producto (modal)</h3>
      <div class="card d-flex flex-row text-white bg-dark" >
        <img class="card-img-top card-img" src="https://media.pitchfork.com/photos/6384d8132433cfb2d45c761a/4:3/w_2664,h_1998,c_limit/Metallica.jpg" alt="Card image cap">
        <div class="d-flex flex-column p-5">
          <div class="card-body">
            <h2 class="card-title">{{ detalle.nombre }}</h2>
            <p class="card-text">En {{ detalle.eventplace }}</p>
            <p class="card-text">Capacidad total {{ detalle.capacity }} / {{ detalle.availabletikets }} entradas disponibles</p>
          </div>
          <ul class="list-group list-group-flush text-dark">
            <li class="list-group-item">Fecha: {{ detalle.fecha }}</li>
            <li class="list-group-item">Apertura puertas: {{ detalle.doorsopenat }}</li>
            <li class="list-group-item">Valor: £ {{ detalle.precio }}</li>
          </ul>
          <div class="card-body">
            <p>{{ detalle.description }}</p>
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
