<template>
  <div class="mt-5 componente">
    <h3>Ejemplo vista carrito</h3>
    <table class="table table-dark mt-2">
      <thead>
        <tr>
          <th scope="col">Evento</th>
          <th scope="col">Fecha</th>
          <th scope="col">Precio</th>
          <th scope="col">Cantidad</th>
          <th scope="col">Total</th>
          <th scope="col">Agregar/Eliminar</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(producto, index) of misProductos" :key="index">
          <td>{{producto.nombre}}</td>
          <td>{{producto.fecha}}</td>
          <td>{{producto.precio}}</td>
          <td>1</td>
          <td>{{producto.precio }}</td>
          <td><button class="btn btn-success mr-2">+</button>
            <button class="btn btn-danger">-</button></td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'MyCart',
  props: {
    misProductos: Array,

  }, data(){
   return {
    total: this.producto.precio
   }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.componente{
  width: 700px;
  
}
.card-img{
  object-fit: cover; 
  height: 250px;
}
</style>
