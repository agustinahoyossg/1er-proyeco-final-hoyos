<template>
  <div class="componente-login m-5">
    <h3 class="title-margin" >Bienvenido de nuevo! Ingresa para adquirir tus tickets</h3>
  <form id="formulario-login" action="" @submit.prevent="validarUsuario">
    <div class="input-group mb-3">
    
      <input type="email" v-model="email" class="form-control" placeholder="Usuario" aria-label="Usuario" aria-describedby="basic-addon1">
    </div>   
    <div class="input-group mb-3">
      <input type="password" v-model="password" class="form-control" placeholder="Contraseña" aria-label="Contraseña" aria-describedby="basic-addon2">
    </div>
    <div class="input-group mb-3">
      <input type="submit" class="btn btn-warning" value="Ingresar" aria-label="Login" aria-describedby="basic-addon2"/>
     
    </div>
  </form>
  <div>
   <h5> Usario de prueba: </h5> 
   <p>
    email: matilde@usuaria.com password: usu23
   </p> 
   <h5> Admin de prueba: </h5> 
   <p>
    email: admin@eventos.com password:abc123
   </p> 
  </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'LoginComponent',
  props: {
    
  },
  data() {
    return {
      usuarios: [],
      email: '',
      password: '',
      existeUsuario: false,
      existeAdmin: false,
    }
  },
   created(){
    const URLGET = "https://63a21bbcba35b96522f039e2.mockapi.io/londonevents/users"
            axios.get(URLGET)
            .then((response) => {
              this.usuarios = response.data
            })
           .catch((err) => {console.error(`${err}`)})
        },
    methods: {
      validarUsuario(){
       const usuarioIngresado = this.usuarios.filter(usuario => usuario.email === this.email && usuario.password === this.password)
     if (usuarioIngresado.length === 1 ){
      if (this.email === "admin@eventos.com" ){
        this.$router.push('admin')

      } else this.$router.push('user')
      }
      else {
        alert("El usuario no existe, por favor registrate")
      }
      }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.componente-login{
  width: 600px;
}
.title-margin {
  margin-bottom: 45px;
}
</style>
