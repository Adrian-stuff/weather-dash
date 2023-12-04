<script lang="ts">
	import { onMount } from 'svelte';

	let weather: HTMLIFrameElement;

	onMount(async () => {
		// weather.onload = () => {
		// 	let we = document.getElementsByClassName('MjjYud')[0].innerHTML;
		// 	console.log(we);
		// };
		window.open(
			'https://zoom.earth/maps/satellite/#view=13.786,122.04,6z/date=2023-11-18,13:30,+8/overlays=radar,wind',
			'_blank',
			'width=500,height=500,left=500,top=0'
		);
	});
</script>

<iframe
	width="650"
	height="650"
	src="https://embed.windy.com/embed2.html?lat=14.662&lon=120.949&detailLat=14.650&detailLon=121.050&width=650&height=650&zoom=11&level=surface&overlay=rain&product=ecmwf&menu=&message=true&marker=&calendar=now&pressure=&type=map&location=coordinates&detail=&metricWind=default&metricTemp=default&radarRange=-1"
	frameborder="0"
	title="satellite"
></iframe>
<iframe
	class="google-weather"
	bind:this={weather}
	src=""
	title="weather"
	frameborder="0"
	width="700"
	height="650"
>
</iframe>
<iframe
	src="https://www.rainviewer.com/map.html?loc=15.0827,121.02,7&oFa=0&oC=1&oU=0&oCS=1&oF=0&oAP=1&c=5&o=83&lm=1&layer=sat-rad&sm=1&sn=0&hu=false"
	width="600"
	height="650"
	frameborder="0"
	allowfullscreen
	title="rainviewer"
></iframe>
<iframe
	class="google-weather scale-50"
	bind:this={weather}
	src="https://www.google.com/search?igu=1&amp;q=punturin+weather"
	title="weather"
	frameborder="0"
	width="700"
	height="650"
>
</iframe>
