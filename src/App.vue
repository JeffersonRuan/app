<template>

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


export default {
  name: 'App',
  components: {

  },
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

</style>
