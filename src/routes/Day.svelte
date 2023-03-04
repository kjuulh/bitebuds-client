<script lang="ts">
	import DayContentCollapsed from './DayContentCollapsed.svelte';
	import DayContentExpanded from './DayContentExpanded.svelte';

	export let day: string;
	export let next = false;
	export let last = false;

	let expanded = false;
</script>

<div class="sm:grid grid-cols-[1fr,4fr] gap-4 space-y-4 sm:space-y-0">
	<div class="relative">
		{#if !last}
			<div class="bg-gray-300 absolute top-3 left-[3px] h-full w-0.5 hidden sm:block z-0" />
		{/if}
		<div class="col-start-1 flex space-x-2">
			<div
				class={`hidden sm:block w-2 h-2 rounded-full mt-2.5 z-10 ${
					next ? 'bg-orange-600' : 'bg-gray-300'
				}`}
			/>
			<div class="inline-block">
				<span class={`text-md font-medium ${next ? 'text-orange-600' : 'text-gray-700'}`}>
					{day}
				</span>
				<p class="text-xs font-normal text-gray-500">2023-03-04</p>
			</div>
		</div>
	</div>
	<div class="col-start-2 transition-all sm:pb-6">
		{#if expanded}
			<DayContentExpanded />
		{:else}
			<DayContentCollapsed
				on:readMore={(_) => {
					expanded = !expanded;
				}}
			/>
		{/if}
	</div>
</div>

<div class="divider block sm:hidden h-0.5 w-full bg-gray-300 my-6 rounded-full" />
