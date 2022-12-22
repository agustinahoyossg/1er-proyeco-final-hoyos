<template>
    <div class="container"> 
        <form @submit.prevent="postEvent()">
            <label>Nombre del evento</label>
            <input v-model="nombre" type="text" class="form-control"/>
            <label>Lugar del evento</label>
            <input v-model="lugar" type="text" class="form-control"/>
            <label>Fecha del evento</label>
            <input v-model="fecha" type="text" class="form-control"/>
            <label>Valor de la entrada</label>
            <input v-model="valor" type="number" class="form-control"/>
            <label>Localidades totales</label>
            <input v-model="localidadestot" type="number" class="form-control"/>
            <label>Localidades disponibles</label>
            <input v-model="localidadesdisp" type="number" class="form-control"/>
            <label>Descripcion</label>
            <input v-model="descripcion" type="text" class="form-control"/>
            <label>Horario de apertura</label>
            <input v-model="apertura" type="text" class="form-control"/>
            <label>Link de la imagen</label>
            <input v-model="imagen" type="text" class="form-control"/>
            <button class="btn btn-success" type="submit">Agregar evento</button>
        </form>

        <form @submit.prevent="deleteEvent()">
            <label>Id del producto a eliminar</label>
            <input v-model="eliminar" type="number" class="form-control"/>
            <button class="btn btn-danger" type="submit">Eliminar evento</button>
        </form>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    name: 'AddProduct',
    data() {
        return {
            nombre: '',
            lugar:'',
            fecha:'',
            valor: null,
            localidadestot: null,
            localidadesdisp: null,
            descripcion:'',
            apertura:'',
            imagen:'',
            eliminar: null
        }
    }, 
    methods: {
        async postEvent() {
            const newEvent = {
                date:this.fecha,
                name: this.nombre,
                image:this.imagen,
                price: this.valor,
                eventplace: this.lugar,
                description:this.descripcion,
                capacity: this.localidadestot,
                availabletickets: this.localidadesdisp,
                doorsopenat:this.apertura,

            }
            const URLPOST = "https://63a21bbcba35b96522f039e2.mockapi.io/londonevents/events"
            axios.post(URLPOST, newEvent)
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





