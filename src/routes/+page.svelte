<script lang="ts">
	import { days } from '$lib/types';
	import { writable } from 'svelte/store';
	import DaySelector from './DaySelector.svelte';
	import TodoItem from './TodoItem.svelte';

	const sundaySelectedDay = new Date().getDay();
	let selectedDay = sundaySelectedDay === 0 ? 6 : sundaySelectedDay - 1;

	const todos = writable([]);

	interface Todo {
		days: string[];
	}
</script>

<div class="w-2/3 md:w-1/2 lg:w-1/3 h-2/3">
	<div
		class="flex items-center content-center justify-between p-2 pl-4 my-2 rounded-md bg-zinc-900"
	>
		<h2 class="text-4xl font-semibold leading-tight align-middle">{days[selectedDay]}</h2>
		<button class="w-16 h-16 text-4xl rounded-md bg-sky-600 hover:bg-sky-500">+</button>
	</div>
	<ul class="w-full h-full p-5 m-auto rounded-md bg-zinc-900">
		<TodoItem title="One" />
		<TodoItem title="Two" />
		<TodoItem title="Three" />
	</ul>
</div>

<DaySelector bind:selected={selectedDay} />
