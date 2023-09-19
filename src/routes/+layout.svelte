<script>
	import '@fontsource/poppins/400.css';
	import '@fontsource/poppins/600.css';
	import '@fontsource/poppins/700.css';
	import '../app.css';
</script>

<div class="w-screen h-screen text-white bg-zinc-950">
	<a href="/">
		<h1 class="absolute left-0 right-0 m-4 text-2xl font-bold text-center">Weekday Todos</h1>
	</a>
	<div
		class="flex flex-col items-center self-center justify-around w-full h-full gap-2 text-center"
	>
		<slot />
	</div>
</div>
