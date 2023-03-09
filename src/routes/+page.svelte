<script lang="ts">
	import Day from './Day.svelte';
</script>

<main class="space-y-4 pt-8">
	<ul class="days flex flex-col">
		<li><Day day="monday" next={true} /></li>
		<li><Day day="tuesday" /></li>
		<li><Day day="wednesday" /></li>
		<li><Day day="friday" last={true} /></li>
	</ul>
</main>
