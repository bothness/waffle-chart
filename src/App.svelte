<script>
	import data from "./data";
	import GridChart from "./GridChart.svelte";
</script>

Rectangular waffle chart (25 X 4)
<div class="wide">
	<GridChart {data} width={4}/>
</div>

Rectangular waffle chart (20 X 5)
<div class="narrow">
	<GridChart {data} width={5} height={100}/>
</div>

Square waffle chart, horizontal bands
<div class="square">
	<GridChart {data} vertical={false} width={10} height={200}/>
</div>

As above, with circular cells
<div class="square">
	<GridChart {data} vertical={false} width={10} height={200} round={true}/>
</div>

<style>
	.wide {
		width: 500px;
		margin-bottom: 20px;
	}
	.narrow {
		width: 400px;
		margin-bottom: 20px;
	}
	.square {
		width: 200px;
		margin-bottom: 20px;
	}
	.legend {
		width: 400px;
		margin-top: 3px;
		margin-bottom: 20px;
	}
</style>