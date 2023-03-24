<script>
	/** @type {import('./$types').PageData} */
	export let data;
</script>

<div>
	<div class="font-bold text-2xl mb-4">Server Side Rendering</div>
	<div class="opacity-80 mb-4">
		This page is returning the date from a SvelteKit page endpoint with no configuration specified.
		This means that when deployed to Vercel, it uses the project default which will automatically
		turn page endpoints into server routes.
	</div>
	<div class="opacity-80 mb-4">
		This page endpoint runs on the server, and returns the current date and time. Notice each time
		you refresh the page, the endpoint runs again and the time is updated.
	</div>
	<div class="bg-zinc-900/60 rounded-md p-6 shadow-md  shadow-zinc-700/30">
		<div class="mb-2 text-sm uppercase text-white/60">Current Date:</div>
		<div class="text-2xl">
			{data.generatedAt}
		</div>
	</div>
</div>
