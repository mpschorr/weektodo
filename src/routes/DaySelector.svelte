<script lang="ts">
	import SquareDayButton from './SquareDayButton.svelte';
	export let selected: number = -1;
</script>

<div class="grid grid-cols-3 col-auto gap-2 sm:grid-cols-5 md:grid-cols-7 lg:grid-cols-7">
	{#each { length: 7 } as _, i}
		<SquareDayButton day={i} bind:selected />
	{/each}
</div>
