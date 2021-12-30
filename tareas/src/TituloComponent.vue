<template>
  <div>
    <h2>{{ tituloMayusculas() }}</h2>
  </div>
</template>

<script>
import { bus } from './main.js'

export default {
  props: ['titulo'],
  data(){
    return {
      numTareas : 0
    }
  },
  methods: {
    tituloMayusculas(){
      return this.titulo.toUpperCase();
    }
  }
}

</script>
