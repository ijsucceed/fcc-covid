<script>
import CovidChart from "../components/CovidChart.svelte";
import CovidStat from "../components/CovidStat.svelte";
import TableContainer from "../components/TableContainer.svelte";
</script>

<svelte:head>
	<title>Covid 19 US Tracker</title>
</svelte:head>

<section class="header">
	<div class="container">
		<h1>Covid 19 - US Tracker</h1>
	</div>
</section>

<CovidStat />
<CovidChart />
<TableContainer />
	