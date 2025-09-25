<template>
<div class="d-flex">
    <!-- Barra Lateral -->
  <div class="d-flex flex-column flex-shrink-0 p-3 text-white bg-dark" style="width: 280px;">
      <BarraLateral />
    
      <hr>
      </div>
    <!-- Formulário --> 
     <div class="flex-grow-1 p-3">
      <Formulario />
     </div>
   
</div>   
       
</template>

<script setup lang="ts">
import BarraLateral from './components/BarraLateral.vue';
import Formulario from './components/Formulario.vue';
</script>


<style scoped>

</style>