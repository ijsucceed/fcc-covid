<script context="module">
	import requests from '../data/requests.js';

	export async function preload() {
		try {
			const usStats = await requests.usStats();
			const historic = await requests.historicUS();

			return { usStats, historic };
		} catch(e) {
			this.error(
				500,
				"There was an error in calling the api, please try again in 5 minutes."
			);
			return;
		}
	}
</script>

<script>
import CovidChart from "../components/CovidChart.svelte";
import CovidStat from "../components/CovidStat.svelte";
import TableContainer from "../components/TableContainer.svelte";

export let usStats;
export let historic;
console.log(historic, 'some history');
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

<CovidStat {...usStats} />
<CovidChart />
<TableContainer />
	