<template>
    <div id="app">
        <Todos v-bind:todos="todos" v-on:del-todo="delTodo"/>
    </div>
</template>

<script>
import Todos from './components/Todos.vue'

export default {
    name: 'app',
    components: {
        Todos
    },
    data () {
        return {
            todos: [
                {
                    id: 1,
                    title: "Hello 1!",
                    completed: false
                },
                {
                    id: 2,
                    title: "Hello 2!",
                    completed: true
                },
                {
                    id: 3,
                    title: "Hello 3!",
                    completed: false
                }
            ]
        }
    },
    methods: {
        delTodo(id) {
            this.todos = this.todos.filter(todo => todo.id !== id)
        }
    }
}
</script>

<style>
    *{
        box-sizing: border-box;
        margin: 0;
        padding: 0;
    }
    body{
        font-family: arial;
    }
</style>
