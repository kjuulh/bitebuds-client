<script lang="ts">
	import { createEventDispatcher } from 'svelte';

	let image =
		'https://images.unsplash.com/photo-1677864234709-bde08838fb9d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=400&q=80';

	const dispatch = createEventDispatcher();

	function readMore() {
		dispatch('readMore', {});
	}
</script>

<article class="day-content grid grid-cols-[30%,70%] space-x-6">
	<img src={image} alt="no alt text supported" class="object-cover" />
	<div class="day-content__body flex flex-col">
		<h2 class="font-semibold text-lg text-orange-600">Pizza</h2>
		<p class="font-normal text-sm">
			Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint consectetur
			cupidatat.
		</p>
		<div class="flex-grow" />
		<button
			class="transition-all h-3 w-20 bg-gray-200 hover:bg-gray-300 self-center rounded-b-[4rem] rounded-t-[1rem] mt-3"
			on:click={() => readMore()}
		/>
	</div>
</article>

