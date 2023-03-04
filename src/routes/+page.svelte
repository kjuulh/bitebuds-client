<script lang="ts">
	import Day from './Day.svelte';
</script>

<main class="space-y-4 pt-8">
	<div class="flex space-x-2 hidden">
		<a class="underline" href="prev">Prev</a>
		<p>9</p>
		<a class="underline" href="next">Next</a>
	</div>

	<ul class="days flex flex-col">
		<li><Day day="monday" next={true} /></li>
		<li><Day day="tuesday" /></li>
		<li><Day day="wednesday" last={true} /></li>
	</ul>
</main>

