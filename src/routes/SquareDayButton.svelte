<script lang="ts">
	import { days } from '$lib/types';
	import { twMerge } from 'tailwind-merge';
	export let selected: number;
	export let day: number;
</script>

<button on:click={() => (selected = day)}
	><div
		class={twMerge(
			'flex items-center justify-center w-24 h-24 p-2 font-bold transition-colors rounded-md cursor-pointer',
			selected == day ? 'bg-sky-600 hover:bg-sky-500' : 'bg-zinc-900 hover:bg-zinc-800'
		)}
	>
		<p class="text-3xl text-white align-middle select-none">
			{days[day].substring(0, 3)}
		</p>
		<!-- <p class="text-3xl text-white align-middle select-none">{day}</p> -->
	</div>
</button>
