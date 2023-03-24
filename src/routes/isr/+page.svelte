<script>
	/** @type {import('./$types').PageData} */
	export let data;
</script>

<div>
	<div class="font-bold text-2xl mb-4">Incremental Static Regeneration</div>
	<div class="opacity-80 mb-4">
		This page is returning the date from a SvelteKit page endpoint with ISR configuration specified.
		Vercel supports Incremental Static Regeneration (ISR), which provides the performance and cost
		advantages of prerendered content with the flexibility of dynamically rendered content.
		Basically, after the page is initially generated, the server will consider the page "stale" and
		in need of regeneration after a certain amount of time has passed.
	</div>
	<div class="opacity-80 mb-4">
		This page endpoint runs on the server, and returns the current date and time. Since it is
		configure to be ISR and it's expiration is set to ten seconds, you'll notice the date does not
		change until at least ten seconds has passed.
	</div>
	<div class="bg-zinc-900/60 rounded-md p-6 shadow-md  shadow-zinc-700/30">
		<div class="mb-2 text-sm uppercase text-white/60">Current Date:</div>
		<div class="text-2xl">
			{data.generatedAt}
		</div>
	</div>
</div>
