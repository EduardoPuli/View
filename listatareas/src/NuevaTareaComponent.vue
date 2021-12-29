<template>
    <div class="imput-group ">
        <input type="text" placeholder="Escribe nueva tarea" v-model="nuevaTarea" class="form-control" @keyup.enter="agregarTarea">
        <span class="input-group-btn pull-right" style="transform-origin: 0 -30px">
        <button type="button" v-on:click="agregarTarea()" class="btn btn-primary"> Agregar</button>
        </span>
    </div>
</template>

<script>
import {bus} from './main.js'

export default {
    data(){
        return{
            nuevaTarea: ''
        }
    },
    props: ['tareas','actualizarContador'],
    methods:{
        agregarTarea(){ 
            var texto = this.nuevaTarea.trim();
            if(texto){
                this.tareas.push({
                    texto: texto,
                    terminada: false 
                })
               // this.actualizarContador();
               bus.actualizarContador(this.tareas.length)
            }
            this.nuevaTarea = '';
        }
    },
    created(){
         bus.actualizarContador(this.tareas.length) 
    }
}
</script>