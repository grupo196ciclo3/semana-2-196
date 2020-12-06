<template>
  
          <div class="card border border-success h-100 pt-4">
            <div class="d-flex justify-content-center p-3">
              <img class="img-fluid" v-bind:src="partes.image" alt="imagenrespectiva">
            </div>
            <div class="card-body">
              <h5 class="card-title text-height-bold">{{partes.titulo}}</h5>
              <p class="card-text">{{partes.descripcion}}</p>
              <a :href="partes.url" class="btn btn-success">{{partes.boton}}</a>
            </div>
          </div>
        
</template>

<script>
export default {
  name: "ComponenteServicios",
  props:{
      "partes":Object
  }
};  
</script>

<style lang="stylus" scoped> 

</style>
