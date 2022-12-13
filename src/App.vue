<template>
  <div id="app">
    <div class="app-margin ">
      <h1 class="text-warning">Best London Gigs</h1>
      <h3>Los mejores eventos de metal y techno en Londres</h3>
   <LoginComponent titulo="Login"/>
    <RegistrationComponent titulo="Registro"/>
    <h3 class="text-left">Lista de productos</h3>
      <div class="cards-wrapper">
        <ProductList  v-for="(producto,index) of productos" :key="index" :nombre="producto.nombre" :precio="producto.precio" :imagen="producto.imagen" :fecha="producto.fecha" :lugar="producto.lugar"
        />
      </div>
      <cart :mis-productos="misProductos"/>
      <ProductDetail :detalle="misProductos[0]" />
    </div>
  </div>
</template>

<script>
import LoginComponent from './components/LoginComponent.vue'
import RegistrationComponent from './components/RegistrationComponent.vue'
import ProductList from './components/ProductList.vue';
import Cart from './components/Cart.vue';
import ProductDetail from './components/ProductDetail.vue';

export default {
  name: 'App',
  components: {
    LoginComponent,
    RegistrationComponent,
    ProductList,
    Cart,
    ProductDetail
  }, 

  data: function() {
    return {
      productos:[
        { nombre: "Napalm Death",
          precio: 60,
          imagen: "https://napalm-death-merchandising.com/media/image/f3/88/e1/napalm_death_1920x1920.jpg",
          fecha: "22/12/2022",
          disponibilidad: 700,
          lugar: "Electric Ballroom",
          descripcion: ""
          
      },
      { nombre: "Animals as Leaders",
          precio: 44,
          imagen: "https://i.scdn.co/image/ab6761610000e5eb720141a7b1a39da1cfa735a5",
          fecha: "13/12/2022",
          disponibilidad: 250,
          lugar: "Undead Club",
          descripcion: ""

      },
      { nombre: "DNB Christmas Party",
          precio: 12,
          imagen:"https://d31fr2pwly4c4s.cloudfront.net/c/3/c/1496881_0_housetechno-refreshers-session-last-free-tickets_1024.jpg",
          fecha: "16/12/2022",
          disponibilidad: 100,
          lugar: "Fire & Lightbox",
          descripcion: ""
        
      },
      ],
      misProductos: [
        
        { nombre: "Napalm Death",
          precio: 60,
          imagen: "https://napalm-death-merchandising.com/media/image/f3/88/e1/napalm_death_1920x1920.jpg",
          fecha: "22/12/2022",
          disponibilidad: 100,
          apertura: "19.30 hs",
          lugar: "Electric Ballroom",
          capacidad: 600,
          descripcion: "Napalm Death vuelve a su ciudad favorita para presentar su nuevo disco. La banda telonera será Symbolic Rituals, tributo a Death."
      },
      { nombre: "Animals as Leaders",
          precio: 44,
          imagen: "https://i.scdn.co/image/ab6761610000e5eb720141a7b1a39da1cfa735a5",
          fecha: "13/12/2022",
          apertura: "19 hs",
          disponibilidad: 250,
          capacidad:600,
          lugar: "Undead Club",
          descripcion: "Los americanos se presentaran por primera vez en el mitico club Undead de Londres, buscando ampliar sus filas para salir del elitismo en que a veces los han encerrado, como creadores de musica para musicos."
      },
      ]

    
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #76808a;
  padding: 60px;
  background-color: #111112 ;
}
.app-margin{
  margin-left: auto;
  margin-right: auto;
}
.cards-wrapper {
  display: flex;
}
</style>
