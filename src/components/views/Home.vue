<template>
	<div id="home">
	<AddTodo v-on:add-todo="addTodo" />
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
	</div>
</template>

<script>
	import AddTodo from '../AddTodo';
	import Todos from '../Todos';

	export default {
	name: 'Home',
	components: {
	  Header,
	  AddTodo,
	  Todos
	},
	data(){
	  return{
	    todos: [
	      {
	        id:1,
	        title: "Todo one",
	        completed: false
	      },
	      {
	        id:2,
	        title: "Todo two",
	        completed: false
	      },        
	      {
	        id:3,
	        title: "Todo three",
	        completed: false
	      },
	    ]
	  }
	},
	methods: {
	  deleteTodo(id){
	    this.todos = this.todos.filter(todo => todo.id !== id);
	  },
	  addTodo(newTodo){
	    this.todos = [...this.todos, newTodo];
	  }
	},
	created(){

	}
	}
</script>