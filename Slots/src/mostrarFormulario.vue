<template>
  <form class="form">
      <slot name="titulo"></slot> 
      <slot name="elementos"></slot> 
  </form>
</template>

<script>
import MostrarFormulario from './mostrarFormulario.vue'
export default {
    components:{
        mostrarFormulario: MostrarFormulario
    }
}
</script>

<style scoped>
</style>