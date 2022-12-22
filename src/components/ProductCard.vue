<template>
  <div class="m-3">
    <div class="cards-container"> 
      <div class="card" style="width: 22rem;" >
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
          <button href="#" class="card-link btn btn-primary" >+ Info</button>
          <button class="card-link btn btn-warning"><svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" fill="currentColor" class="bi bi-cart" viewBox="0 0 16 16">
            <path d="M0 1.5A.5.5 0 0 1 .5 1H2a.5.5 0 0 1 .485.379L2.89 3H14.5a.5.5 0 0 1 .491.592l-1.5 8A.5.5 0 0 1 13 12H4a.5.5 0 0 1-.491-.408L2.01 3.607 1.61 2H.5a.5.5 0 0 1-.5-.5zM3.102 4l1.313 7h8.17l1.313-7H3.102zM5 12a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm7 0a2 2 0 1 0 0 4 2 2 0 0 0 0-4zm-7 1a1 1 0 1 1 0 2 1 1 0 0 1 0-2zm7 0a1 1 0 1 1 0 2 1 1 0 0 1 0-2z"/>
          </svg>Añadir</button>
        </div>
      </div>
    </div>
   
  </div>
</template>

<script>
export default {

  name: 'ProductCard',
  data() {
    return {
        modal: false,
  
    };
  },
  props: {
    nombre: String,
    precio: Number,
    imagen: String,
    fecha: String,
    lugar: String,
    descripcion : String,
    puertas : String,
    localidades : Number,
    capacidadtotal : Number,
    id: Number,
  
  }, 

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.card-img{
  object-fit: cover; 
  height: 250px;
}
.btn {
  font-size: 22px !important;

}
svg {
  margin-right: 10px;
  margin-bottom:2px;
}
</style>
