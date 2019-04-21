<template>
	<nav class="navbar navbar-default">
      <div class="navbar-header">
        <a href="#/" class="navbar-brand">Belajar VueJS</a>
      </div>
      <!-- <div class="container-fluid">
      	<ul class="nav navbar-nav navbar-right">
      		<li><a href="#">About</a></li>
      	</ul>
      </div> -->
    </nav>
</template>

<script>
	export default{
		name: 'Header'
	}
</script>

<style scoped>
	.navbar-default .navbar-brand:hover {
	    color: #fff;
	    background-color: transparent;
	}
	.navbar-default .navbar-nav > li > a {
    	color: #fff;
	}
</style>