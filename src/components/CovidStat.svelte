<script>
    export let cases;
    export let deaths;
    export let recovered;
    export let updated;
    export let hospitalized;
    export let ventilator;
    export let icu;
    export let tested;
</script>

<style>
    .column {
        border: 1px solid #444;
    }
</style>

<div class="section">
    <div class="container">
        <div class="columns">
            <h1 class="is-3 column">Cases: {cases}</h1>
            <h1 class="is-3 column">Deaths: {deaths}</h1>
            <h1 class="is-3 column">Recovered: {recovered}</h1>
            <h2 class="is-3 column">Tested: {tested}</h2>
        </div>
    </div>
</div>

<div class="section">
    <div class="container">
      <div class="columns">
        <h2 class="is-3 column">Hospitalized: {hospitalized}</h2>
        <h2 class="is-3 column">Total ICU: {icu}</h2>
        <h2 class="is-3 column">Total Ventilator: {ventilator}</h2>
        <h1 class="is-3 column">Updated: {updated} </h1>
      </div>
    </div>
</div>