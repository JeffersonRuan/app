<template>
    <div>
       

    </div>
</template>

<script>
export default {
    name: 'App',
    data() {
        return {
            name: 'Jon Snow',
        }
    },

    // Criação
        // Preparar o componente
        // Ajax, inicializar algumas variáveis
        // Não tem acesso ao template (DOM)
    // Montagem
        // Inicializar uma lib externa (new lib())
        // Precisa de acesso ao template (DOM)
        // Tem acesso ao template (DOM)
    // Atualização
        // Debug
        // Update
    // Desmontagem
        // Remover tudo o que for necessário (lib->destroy())
        // Para liberar memória
    
    // HOOKS
    beforeCreate() {
        console.log('beforeCreate');
        console.log(this.name);
    },
    created() {
        console.log('Created');
        console.log(this.name);
    },
    beforeMount() {
        console.log('beforeMount');
        console.log(this.name);
    },
    mounted() {
        console.log('Mounted');
        console.log(this.name);
    },
    beforeUnmount() {
        console.log('beforeUnmount');
    },
    unmounted() {
        console.log('Unmounted');
    },

    watch: {
        
    },

    computed: {

    },

    methods: {
        
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