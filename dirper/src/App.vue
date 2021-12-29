<template>
  <div class="container">
    <div class="jumbotron">
      <span v-decorar:pequeno.italico.negrilla="{familia: 'helvetica', color: 'red'}">Aprende Vue.js 2 Facilmente</span>  
      <hr>
      <span v-decorar-local:grande.bold.italico="{familia: 'serif', color: 'green'}">Aprende Angular 2 Facilmente</span>
    </div> 
  </div>
</template>

<script>
export default {
  directives:{
    'decorar-local' : {
      bind(el, binding, vnode){
    el.style.fontFamily = binding.value.familia;
    el.style.color = binding.value.color;

    if(binding.arg == 'grande'){
      el.style.fontSize ='50px'
    }
    if(binding.arg == 'pequeno'){
      el.style.fontSize ='10px'
    }

    if(binding.modifiers['negrilla']){
      el.style.fontWeight= 'bold';
    }
    if(binding.modifiers['italico']){
      el.style.fontStyle= 'italic';
    }
    }
    }
  }
}
</script>

<style >

</style>
