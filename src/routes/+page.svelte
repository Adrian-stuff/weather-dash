<script lang="ts">
	import { onMount } from 'svelte';

	let weather: HTMLIFrameElement;

	onMount(async () => {
		// window.open(
		// 	'https://zoom.earth/maps/precipitation/#view=13.786,122.04,6z/model=icon/overlays=radar,wind',
		// 	'_blank',
		// 	'width=500,height=500,left=500,top=0'
		// );
	});
</script>

<title>PSHS Weather Monitoring</title>
<div class="">
	<!-- <h1>For more detailed information:</h1> -->
	<ul class="flex flex-row w-full">
		<a
			class="p-5 bg-blue-200 hover:bg-blue-300 flex-grow text-center hover:cursor-pointer"
			target="_blank"
			href="https://zoom.earth/maps/satellite/#view=14.7786,121.4294,7z/overlays=radar,wind"
		>
			<li class="font-sans text-2xl text-gray-800 heading">Zoom Earth Live Satellite</li>
		</a>
		<a
			class="p-5 bg-blue-200 hover:bg-blue-300 flex-grow text-center hover:cursor-pointer"
			target="_blank"
			href="https://zoom.earth/maps/satellite/#view=14.7786,121.4294,7z/overlays=radar,wind"
		>
			<li class="font-sans text-2xl text-gray-800 heading">MSN Weather Map</li>
		</a>
		<a
			class="p-5 bg-blue-200 hover:bg-blue-300 flex-grow text-center hover:cursor-pointer"
			target="_blank"
			href="https://zoom.earth/maps/satellite/#view=14.7786,121.4294,7z/overlays=radar,wind"
		>
			<li class="font-sans text-2xl text-gray-800 heading">MSN Weather Forecast</li>
		</a>
	</ul>
</div>
<div class="grid grid-cols-2 gap-2 p-2 [&>*]:border [&>*]:rounded-lg">
	<iframe
		class="w-full overflow-hidden h-screen"
		src="https://embed.windy.com/embed2.html?lat=14.662&lon=120.949&detailLat=14.650&detailLon=121.050&width=650&height=650&zoom=11&level=surface&overlay=rain&product=ecmwf&menu=&message=true&marker=&calendar=now&pressure=&type=map&location=coordinates&detail=&metricWind=default&metricTemp=default&radarRange=-1"
		frameborder="0"
		title="satellite"
	></iframe>

	<iframe
		class="w-full overflow-hidden h-screen"
		src="https://www.rainviewer.com/map.html?loc=15.0827,121.02,7&oFa=0&oC=1&oU=0&oCS=1&oF=0&oAP=1&c=5&o=83&lm=1&layer=sat-rad&sm=1&sn=0&hu=false"
		frameborder="0"
		title="rainviewer"
	></iframe>
	<iframe
		class="w-full overflow-hidden h-screen"
		src="https://www.google.com/search?igu=1&amp;q=punturin+weather"
		title="weather"
		frameborder="0"
		scrolling="no"
	>
	</iframe>
	<iframe
		class="w-full overflow-hidden h-screen"
		src="https://www.bing.com/search?q=weather+punturin&cvid=a291ea8b45ff4095b53b204f192d7608&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIGCAEQLhhAMgYIAhAAGEAyBggDEC4YQDIGCAQQABhAMgYIBRAAGEAyBggGEAAYQDIGCAcQLhhAMgYICBBFGDzSAQgyMDk0ajBqNKgCALACAA&FORM=ANAB01&PC=U531"
		title="weather"
		scrolling="no"
		frameborder="0"
	>
	</iframe>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Passion+One&display=swap');
	.heading {
		font-family: 'Passion One', sans-serif;
	}
</style>
