<template>
	<span v-bind:class="{'is-complete':todo.completed}">
		<input type="checkbox" v-on:change="markComplete">
		{{ todo.title }}
		<span class="badge"@click="$emit('del-todo', todo.id)">&times;</span>
		</span>
	</span>
</template>

<script>
	export default{
		name: 'TodoItem',
		props: ['todo'],
		methods: {
			markComplete(){
				this.todo.completed = !this.todo.completed;
			}
		}
	}
</script>

<style scoped>
	.is-complete{
		text-decoration: line-through;
	}
	.badge{
		background: #ff0000;
		padding: 5px 9px;
		border-radius: 4px;
		cursor: pointer;
		float: right;
	}
</style>