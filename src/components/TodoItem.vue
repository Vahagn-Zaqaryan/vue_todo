<template>
        <div class="card z-depth-1">
          <div class="card-content grey-text text-darken-3">
            <span class="card-title" style="margin: 0;">
                <label>
                    <input type="checkbox" class="filled-in" :checked="todo.completed? true : false " v-on:change="markC"/>
                    <span class="black-text" v-bind:class="{'is-complete': todo.completed}">{{todo.title}}</span>
                </label>
                <button @click="$emit('del-todo', todo.id)" class="del"><i class="material-icons" style="color: #555;">delete</i></button>
            </span>
          </div>
        </div>
</template>

<script>
    export default {
        name: 'TodoItem',
        props: ["todo"],
        methods: {
            markC() {
                this.todo.completed = !this.todo.completed;
            }
        }
    }
</script>

<style scoped>

    .is-complete {
        text-decoration: line-through;
        color: #aaa;
    }
    .del {
        opacity: 0.8;
        background-color: #fff;
        border: none;
        cursor: pointer;
        float: right;
        transition: all .3s;
    }
    .del:hover{
        opacity: 1;
    }
</style>
