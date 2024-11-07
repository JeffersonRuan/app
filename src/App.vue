<template>
  <div>
    <BaseCard />
  </div>

  <div v-show="showUsuario">
    <div v-if="acessLevel === 'admin'">Usuário Admin</div>
    <div v-else-if="acessLevel === 'marketing'">Usuário Marketing</div>
    <div v-else>Usuário normal</div>
  </div>

  <div v-show="showName">
    Nome: {{ firstName }} <br>
    Sobrenome: {{ lastName }}
  </div>

</template>

<script>
import BaseCard from './components/BaseCard.vue';



export default {
  name: 'App',
  components: { BaseCard },
  data() {
    return {
      showHeader: false,
      firstName: 'Jon',
      lastName: 'Snow',
      showName: false,
      showUsuario: false,
      acessLevel: 'admin'
    }
  }
}
</script>

<style>
#app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
        margin: 60px;
    }
</style>
