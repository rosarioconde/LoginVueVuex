<template >
  <div class="home" style="text-align:center">
    <img alt="Vue logo" src="../assets/logo.png">
    <form @submit.prevent="login(usuario)">
      <input type="text" placeholder="Ingrese email" v-model="usuario.email">
      <input type="password" placeholder="Ingrese contraseña" v-model="usuario.password">
      <button type="submit">Acceder</button>
    </form>
    {{usuario}}
  </div>
</template>

<script>
import {mapActions} from 'vuex'
export default {
  data() {
    return {
      usuario: {
        email: 'j828@gmail.com',
        password: '123456'
      }
    }
  },
  methods: {
    ...mapActions(['login'])
  }
}
</script>