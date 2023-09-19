<script lang="ts">
	export let data: DayPageData;
	import { days } from '$lib/types';
	import DaySelector from '../DaySelector.svelte';
	import TodoItem from '../TodoItem.svelte';
</script>

<h2 class="m-2 text-4xl font-semibold">{days[data.day]}</h2>
<ul class="w-2/3 p-5 rounded-md md:w-1/2 lg:w-1/3 h-2/3 bg-zinc-900">
	<TodoItem title="One" />
	<TodoItem title="Two" />
	<TodoItem title="Three" />
</ul>
<DaySelector selected={data.day} />
