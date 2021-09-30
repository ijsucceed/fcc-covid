<script>
	export let segment;
</script>

<nav class="navbar" role="navigation" aria-label="main-navigation">
	<div class="navbar-brand">
		<a href="/" class="navbar-brand-item">
			<img src="logo.png" height="38px" width="38px" alt="Covid 19 Logo">
		</a>

		<span class="navbar-burger" aria-label="menu" aria-expanded="false">
			<span aria-hidden="true"></span>
			<span aria-hidden="true"></span>
			<span aria-hidden="true"></span>
		</span>
	</div>

	<div class="navbar-menu">
		<div class="navbar-start">
			<a class="navbar-item" href="/" aria-current="{segment}">Home</a>
			<a class="navbar-item" href="/about">About</a>
		</div>
	</div>
</nav>