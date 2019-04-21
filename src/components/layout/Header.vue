<template>
	<nav class="navbar navbar-default">
      <div class="navbar-header">
        <a href="#/" class="navbar-brand">TODO VueJS</a>
        <button class="navbar-toggle" data-toggle="collapse" data-target="#navb">
        	<span class="icon-bar"></span>
			<span class="icon-bar"></span>
			<span class="icon-bar"></span>
        </button>
      </div>
      <div class="collapse navbar-collapse" id="navb">
      	<ul class="nav navbar-nav navbar-right">
      		<li><a target="_blank" href="https://zulfizz.github.io">Blog</a></li>
      	</ul>
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
	.navbar-default .navbar-toggle:hover,
	.navbar-default .navbar-toggle:focus{
		background-color: #35495e;
	}
	.navbar-default .navbar-toggle .icon-bar{
		background-color: #fff;
	}
</style>