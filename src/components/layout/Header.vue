<template>
	<nav class="navbar navbar-default">
      <div class="navbar-header">
        <a href="#/" class="navbar-brand">TODO VueJS</a>
      </div>
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
	.navbar{
	  border-radius: 0;
	  background-color: #41b883;
	  color: white;
	}
	.navbar a.navbar-brand{
	  color: white;
	}
</style>