<template>
  <div class="container">
    <div class="jumbotron">
      <mostrarFormulario>

        <div slot="titulo">
          <h3> Cambiar Contraseña </h3>
        </div> 
        
      <div slot="elementos">
        <div class="form-group">
          <label for="correo">Correo Electronico</label>
          <input type="email" class="form-control" id="correo" placeholder="Escribe tu correo electronico">
        </div>
      </div>

    <div slot>
      <button class="btn btn-primary"> Cambiar Contraseña </button>
    </div>

      </mostrarFormulario>
    </div> 
  </div>
</template>

<script>
export default {
    data(){
        return{

        }
    }
}
</script>

<style>

</style>
