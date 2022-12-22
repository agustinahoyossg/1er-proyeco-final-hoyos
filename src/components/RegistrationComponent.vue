<template>
  <div class="componente-login m-5">
    <h3 class="title-margin">Nuevo usuario? Registrate para poder comprar en nuestra tienda</h3>
    <form  @submit.prevent="postUser()">
      <div class="input-group mb-3">
        <input type="text" class="form-control" v-model="nombre" placeholder="Nombre" aria-label="Nombre" aria-describedby="basic-addon1">
      </div>   
      <div class="input-group mb-3">
        <input type="text" class="form-control" v-model="avatar"  placeholder="Avatar(link de imagen)" aria-label="Avatar" aria-describedby="basic-addon1">
      </div>   
      <div class="input-group mb-3">
        <input type="email" class="form-control" v-model="email" placeholder="Usuario (tu email)" aria-label="Usuario" aria-describedby="basic-addon1">
      </div>   
      <div class="input-group mb-3">
        <input type="password" class="form-control" v-model="password"  placeholder="Contraseña" aria-label="Contraseña" aria-describedby="basic-addon2"/>
     </div>
      <div class="input-group mb-3">
        <input type="submit" class="btn btn-warning" aria-label="Registrarse" aria-describedby="basic-addon2"/>
      </div>
    </form>

  </div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'RegistrationComponent',
  data() {
        return {
            nombre: '',
            avatar:'',
            email:'',
            password: null,
        }
    }, 
    methods: {
        async postUser() {
            const newUser= {
                avatar:this.avatar,
                name: this.nombre,
                email:this.email,
                password: this.password,

            }
            const URLPOST = "https://63a21bbcba35b96522f039e2.mockapi.io/londonevents/users"
            axios.post(URLPOST, newUser)
            .then((response) => 
           {console.table(response.data)})
           .catch((err) => {console.error(`${err}`)})
        },

       deleteEvent(){
            const URLDELETE = "https://63a21bbcba35b96522f039e2.mockapi.io/londonevents/events/"+this.eliminar;
            const respuesta = axios.delete(URLDELETE);
            console.log(respuesta)           
        }
    }
}
</script>