<template>
	<div class="container-fluid">
		<form @submit="addTodo" class="form-horizontal">
			<div class="form-group">
				<div class="col-sm-10">
					<input class="form-control" v-model="title" type="text" name="title" placeholder="Tambah Tugas...">
				</div>
				<div class="col-sm-2">
					<input class="btn btn-block" type="submit" value="Tambah">
				</div>
			</div>
		</form>
	</div>
</template>

<script>
	import uuid from 'uuid';
	export default{
		name: 'AddTodo',
		data(){
			return{
				title: ''
			}
		},
		methods: {
			addTodo(e){
				e.preventDefault();
				const newTodo = {
					id : uuid.v4(),
					title: this.title,
					completed: false
				}
				// send up to parent
				this.$emit('add-todo', newTodo);
				this.title = '';
			}
		}
	}
</script>

<style scoped>
	.btn{
		background-color: #35495e;
		color: #fff;
	}
</style>