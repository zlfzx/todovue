<template>
  <div id="app">
    <Header />
    <AddTodo v-on:add-todo="addTodo" />
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
    <router-view/>
  </div>
</template>

<script>
  import Header from './components/layout/Header';
  import AddTodo from './components/AddTodo';
  import Todos from './components/Todos';

  export default {
    name: 'App',
    components: {
      Header,
      AddTodo,
      Todos
    },
    data(){
      return{
        todos: []
      }
    },
    methods: {
      deleteTodo(id){
        this.todos = this.todos.filter(todo => todo.id !== id);
      },
      addTodo(newTodo){
        this.todos = [...this.todos, newTodo];
      }
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
