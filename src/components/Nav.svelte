<script>
	let isOpen = false;
	export let segment;

	function toggleNav() {
		isOpen = !isOpen;
	}
</script>

<style>
	@media(min-width: 769px) {
		nav {
			border-bottom: 1px solid gray;
			margin-bottom: 30px;
		}
	}
</style>

<nav class="navbar" role="navigation" aria-label="main-navigation">
	<div class="navbar-brand">
		<a href="/" class="navbar-item">
			<img src="logo.png" height="38px" width="38px" alt="Covid 19">
		</a>

		<span
			class="navbar-burger"
			aria-label="menu"
			aria-expanded="false"
			on:click={toggleNav}
			class:is-active={isOpen}
		>
			<span aria-hidden="true"></span>
			<span aria-hidden="true"></span>
			<span aria-hidden="true"></span>
		</span>
	</div>

	<div class="navbar-menu" class:is-active={isOpen}>
		<div class="navbar-start">
			<a class="navbar-item" href="/" class:is-active={segment === undefined}>Home</a>
			<a class="navbar-item" href="/about" class:is-active={segment === 'about'}>About</a>
		</div>
	</div>
</nav>