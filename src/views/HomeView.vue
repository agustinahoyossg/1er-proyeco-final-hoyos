<template>
  <div class="container-fluid">
    <div class="contenedor-forms">
        <LoginComponent />
        <registration-component />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import LoginComponent from '@/components/LoginComponent.vue'
import RegistrationComponent from '@/components/RegistrationComponent.vue'

export default {
  name: 'HomeView',
  components: {
    LoginComponent,
    RegistrationComponent
  }
}

//how to goback to last route this.$router.go(-1)
</script>

<style scoped>
.contenedor-forms {
  display: flex;
  margin: auto;
  justify-content: center;
  align-content: flex-start;
}
</style>
