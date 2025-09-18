<template>
<header>
    <h1>
      <img src="/assets/logow.png" alt="logo task tracker">  Task Tracker
    </h1>
  <ul>
    <li><FontAwesomeIcon :icon="faHouse" size="2x" /> <a href="/"> Início</a></li>
    <li><FontAwesomeIcon :icon="faUser" size="2x" /> <a href="/"> Perfil</a></li>
    <li><FontAwesomeIcon :icon="faGears" size="2x" /> <a href="/"> Configurações</a></li>
    <li><FontAwesomeIcon :icon="faListCheck" size="2x" /><a href="/"> Tarefas</a></li>
    
  </ul> 
</header>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { faHouse,faUser, faGears, faListCheck } from '@fortawesome/free-solid-svg-icons';

export default defineComponent({
  name: 'BarraLateral',
  components: {
    FontAwesomeIcon
  },
  setup() {
    return {
      faHouse,
      faUser,
      faGears,
      faListCheck
    };
  }
});
</script>


<style scoped>
header {
  padding: 1rem;
  width: 100%;
  height: 100vh;
}
@media only screen and (max-width: 768px) {
  header {
    padding: 2.5rem;
    height: auto;
  }
}
</style>