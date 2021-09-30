<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style lang="scss" global>
	@import "../../node_modules/bulma/bulma.sass";
</style>

<Nav {segment}/>

<slot></slot>