<template>
  <div class="componente-login m-5">
    <h3>{{ titulo }}</h3>
    <div class="input-group mb-3">
      <input type="email" class="form-control" placeholder="Usuario" aria-label="Usuario" aria-describedby="basic-addon1">
    </div>   
    <div class="input-group mb-3">
      <input type="password" class="form-control" placeholder="Contraseña" aria-label="Contraseña" aria-describedby="basic-addon2">
    </div>
    <div class="input-group mb-3">
      <input type="submit" class="btn btn-warning" value="Ingresar" aria-label="Login" aria-describedby="basic-addon2"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LoginComponent',
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
