<template>
   <ul class="list-group">
    <li v-for="(tarea, indice) of tareas" class="list-group-item" :class="{terminada: tareas.terminada}">
        {{ tarea.texto }}
        <span class = "pull-right">
            <button  type="button" class="btn btn-success btn-xs"  @click="tarea.terminada = !tarea.terminada"><i class="bi bi-check-lg"></i></button>
            <button  type="button" class="btn btn-danger btn-xs" @click="borrar(indice)"  ><i class="bi bi-x-lg"></i></button>
        </span>
    </li> 
</ul>
</template>

<script>
export default {
    props: ['tareas'],
    methods:{
        borrar(indice){
            this.tareas.splice(indice,1)
        }
    }
}
</script>

<style scoped>
.terminada{
    color: gray;
    text-decoration: line-through;
}
</style>