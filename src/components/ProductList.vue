<template>
  <div class="m-3">
    <div class="cards-container"> 
      <div class="card" style="width: 18rem;" >
        <img class="card-img-top card-img" :src=this.imagen alt="Card image cap">
        <div class="card-body">
          <h5 class="card-title">{{ nombre }}</h5>
          <p class="card-text">En {{ lugar }}</p>
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">{{ fecha }}</li>
          <li class="list-group-item">Valor: £ {{ precio }}</li>
        </ul>
        <div class="card-body">
          <a href="#" class="card-link btn btn-primary">Ver en mapa</a>
          <a href="#" class="card-link btn btn-warning">Comprar</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductList',
  props: {
    nombre: String,
    precio: Number,
    imagen: String,
    fecha: String,
    lugar: String,

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.card-img{
  object-fit: cover; 
  height: 250px;
}
</style>
