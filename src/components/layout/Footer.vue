<template>
	<footer class="footer navbar navbar-default navbar-fixed-bottom">
		<div class="container">
			<h6 class="text-center">{{ author }}</h6>
		</div>
	</footer>
</template>

<script>
	export default{
		name: 'Footer',
		data(){
			return{
				author: 'Muhammad Zulfi Izzulhaq'
			}
		}
	}
</script>

<style scoped>
.footer{
	min-height: 35px;
	border-radius: 0;
	background-color: #35495e;
	color: white;
}
</style>