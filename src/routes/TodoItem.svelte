<script lang="ts">
	export let title: string;
	export let done: boolean = false;
</script>

<li class="flex justify-between p-2 m-1 text-xl rounded-md bg-zinc-800">
	<input
		type="checkbox"
		class="w-8 h-8 border-none rounded-md outline-none appearance-none cursor-pointer bg-zinc-700 text-zinc-300 focus:ring-0 focus:outline-none focus:text-primary focus:ring-offset-0"
		bind:checked={done}
	/>
	<p class="pr-2 font-semibold text-semibold">{title}</p>
</li>
