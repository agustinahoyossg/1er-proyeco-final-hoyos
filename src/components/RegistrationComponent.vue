<template>
  <div class="componente-login m-5">
    <h3>{{ titulo }}</h3>
    <h5>Registrate para poder comprar en nuestra tienda</h5>
    <div class="input-group mb-3">
      <input type="text" class="form-control" placeholder="Nombre" aria-label="Nombre" aria-describedby="basic-addon1">
    </div>   
    <div class="input-group mb-3">
      <input type="text" class="form-control" placeholder="Apellido" aria-label="Apellido" aria-describedby="basic-addon1">
    </div>   
    <div class="input-group mb-3">
      <input type="date" class="form-control" placeholder="Fecha de Nacimiento" aria-label="Fecha" aria-describedby="basic-addon1">
    </div>   
    <div class="input-group mb-3">
      <input type="email" class="form-control" placeholder="Usuario (tu email)" aria-label="Usuario" aria-describedby="basic-addon1">
    </div>   
    <div class="input-group mb-3">
      <input type="password" class="form-control" placeholder="Contraseña" aria-label="Contraseña" aria-describedby="basic-addon2"/>
   </div>
    <div class="input-group mb-3">
      <input type="password" class="form-control" placeholder="Repetir Contraseña" aria-label="Rcontraseña" aria-describedby="basic-addon2"/>
    </div>
    <div class="input-group mb-3">
      <input type="submit" class="btn btn-warning" aria-label="Registrarse" aria-describedby="basic-addon2"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RegistrationComponent',
  props: {
    titulo: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.componente-login{
  width: 500px;
  
}

</style>
