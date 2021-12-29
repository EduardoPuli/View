<template>
  <div class="container">
    <div class="jumbotron">
      <mostrarFormulario>

        <div slot="titulo">
          <h3> Iniciar Sesion </h3>
        </div> 
        
      <div slot="elementos">
        <div class="form-group">
          <label for="correo">Correo Electronico</label>
          <input type="email" class="form-control" id="correo" placeholder="Escribe tu correo electronico">
        </div>
        <div class="form-group">
          <label for="correo">Contraseña</label>
          <input type="email" class="form-control" id="correo" placeholder="Escribe tu correo electronico">
        </div>
      </div>

    <div slot>
      <button class="btn btn-primary"> Iniciar Sesion </button>
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
    },
    destroyed(){
        console.log('El componente fue destruido')
    },
    activated(){
        console.log('El componente fue activado') 
    },
    deactivated(){
        console.log('El componente fue desactivado')
    }
}
</script>

<style>
</style>
