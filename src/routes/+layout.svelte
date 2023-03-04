<script>
	import '../app.css';
</script>

<div class="app grid lg:grid-cols-[25%,50%,25%] sm:grid-cols-[10%,80%,10%] grid-cols-[5%,90%,5%]">
	<main class="main col-start-2">
		<div class="pt-4">
			<h1 class="font-semibold text-xl tracking-wide">Bitebuds</h1>
			<slot />
		</div>
	</main>
</div>
