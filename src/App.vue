<template>
  <!-- <TheHeader /> -->
  <!-- <TwoWay /> -->
  <!-- <EventosJs /> -->
  <!-- <PropComputed /> -->
  <ObsWatch />

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
// import TheHeader from './components/TheHeader.vue';
// import TwoWay from './components/TwoWay.vue';
// import EventosJs from './components/EventosJs.vue'
// import PropComputed from './components/PropComputed.vue';
import ObsWatch from './components/ObsWatch.vue';

export default {
  name: 'App',
  components: {
    // TheHeader,
    // TwoWay,
    // EventosJs,
    // PropComputed,
    ObsWatch
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
