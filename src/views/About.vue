<template>
  <div class="about">
    <h1>Ruta protegida</h1>
    {{token}}
  </div>
</template>
<script>
import { mapState } from "vuex";
export default {
  computed:{
    ...mapState(['token'])
  }
};
</script>