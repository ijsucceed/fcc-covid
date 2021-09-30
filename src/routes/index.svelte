<script context="module">
	import requests from '../data/requests.js';

	export async function preload() {
		try {
			const usStats = await requests.usStats();

			return { usStats };
		} catch(e) {}
	}
</script>

<script>
import CovidChart from "../components/CovidChart.svelte";
import CovidStat from "../components/CovidStat.svelte";
import TableContainer from "../components/TableContainer.svelte";

export let usStats;
console.log(usStats, 'usStats');
</script>

<style>
	h1 {
		color: blue;
	}
</style>

<svelte:head>
	<title>Covid 19 US Tracker</title>
</svelte:head>

<section class="header">
	<div class="container">
		<h1 class="title">Covid 19 - US Tracker</h1>
	</div>
</section>

<CovidStat {...usStats}/>
<CovidChart />
<TableContainer />
	