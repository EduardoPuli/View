<template>
  <div id="app" class="container">
    <div class="jumbotron">
      <titulo :titulo="titulo"></titulo>
      <nueva-tarea :tareas="tareas" ></nueva-tarea>
      <lista-tareas :tareas="tareas"></lista-tareas>
    </div>
  </div>
</template>

<script>
import Titulo from './TituloComponent.vue'
import NuevaTarea from './NuevaTareaComponent.vue'
import ListaTareas from './ListaTareasComponent.vue'

export default {
  components: {
    Titulo,
    NuevaTarea,
    ListaTareas
  },
  data(){
    return {
      titulo : 'Lista de Tareas',
      tareas: []
    }
  },

  created(){
    this.$http.get('tareas.json')
      .then(response => {
        console.log(response.data)
        for (let id in response.data) {
          let tarea = {
            id: id,
            texto: response.data[id].texto,
            terminada: response.data[id].terminada
          };
          this.tareas.push(tarea);
  /* Pasar respuesta a un objeto de tipo json */
      }
    })
  }
}
</script>

<style>

</style>