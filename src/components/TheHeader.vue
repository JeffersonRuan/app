<template>
    <h1 :class="{ 'title': true, 'title-home': isHome}">
        Curso Vue 3
    </h1>

    <p :class="pClass">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam debitis inventore consectetur dicta magnam consequatur eum dolore, autem rem possimus ea ipsa non nihil amet voluptatibus eos natus velit facere.
    </p>

    <p :style="styleClass">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Sit impedit incidunt, quae aliquid qui modi quisquam perferendis enim optio, accusantium alias ducimus doloremque suscipit tempore. Earum maxime in error accusantium?
    </p>

    <div>
        <div 
            v-for="obj, index in todos"
            :key="obj.id"
            class="todos-item"
        >
            <img 
                v-if="obj.imgSrc"
                :src="obj.imgSrc"
            >
            {{ index }} - {{ obj.title }}
        </div>
    </div>
</template>

<script>
    export default {
        name: 'App',
        data() {
            return {
                classVar: 'title',
                isHome: true,
                styleClass: { 'color': 'aqua', 'backgroundColor': 'black', 'font-size': '20px'},
                pClass: ['text', 'text-home'], 
                todos: [
                    {
                        "userId": 1,
                        "id": 1,
                        "title": "delectus aut autem",
                        "completed": false,
                        "imgSrc": "https://via.placeholder.com/150"
                    },
                    {
                        "userId": 1,
                        "id": 2,
                        "title": "quis ut nam facilis et officia qui",
                        "completed": false,
                        "imgSrc": "https://via.placeholder.com/150"
                    },
                    {
                        "userId": 1,
                        "id": 3,
                        "title": "fugiat veniam minus",
                        "completed": false
                    },
                    {
                        "userId": 1,
                        "id": 4,
                        "title": "et porro tempora",
                        "completed": true
                    },
                    {
                        "userId": 1,
                        "id": 5,
                        "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
                        "completed": false
                    }
]
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

    .title {
        font-size: 20px;
        color: blue;
    }

    .title-home {
        font-size: 40px;
        color: green;
    }

    .text {
        color: rgb(142, 230, 139);
    }

    .text-home {
        color: #42b983;
    }

    .todos-item {
        background-color: #000;
        margin: 0 0 5px 0;
        padding: 5px;
        color: #fff;
        border-radius: 10px;
    }


</style>