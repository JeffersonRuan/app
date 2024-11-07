<template>
  <div>
    <BaseAlert 
      v-if="showAlert"
      :variant="variant"
      @close="onClose()"
    >
      {{ text }}
    </BaseAlert>

  
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
import BaseAlert from './components/BaseAlert.vue';

export default {
  name: 'App',
  components: { BaseAlert },
  data() {
    return {
      showHeader: false,
      firstName: 'Jon',
      lastName: 'Snow',
      showName: false,
      showUsuario: false,
      acessLevel: 'admin',
      showAlert: true,
      variant: 'success',
      text: 'Seu formulário foi enviado!'
    }
  },
  methods: {
    onClose() {
      this.showAlert = false;
      console.log('on close')
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
