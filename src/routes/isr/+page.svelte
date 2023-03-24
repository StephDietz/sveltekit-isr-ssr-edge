<script>
	/** @type {import('./$types').PageData} */
	export let data;
</script>

<div>
	<div class="font-bold text-2xl mb-4">Incremental Static Regeneration</div>
	<div class="opacity-80 mb-4">
		This page is returning the date from a SvelteKit page endpoint with ISR configuration specified.
		Incremental Static Regeneration allows you to create or update content without redeploying your
		site. When you deploy a route with ISR, Vercel caches the page to serve it to visitors
		statically, and rebuilds it on a time interval of your choice. ISR has three main benefits for
		developers: better performance, improved security, and faster build times. Learn more about ISR <a
			href="https://vercel.com/docs/concepts/incremental-static-regeneration/overview#"
			target="_blank"
			class="text-blue-400 hover:text-blue-400">here</a
		>.
	</div>
	<div class="opacity-80 mb-4">
		This page endpoint runs on the server, and returns the current date and time. Since it is
		configure to be ISR and it's expiration is set to ten seconds, you'll notice the date does not
		change until at least ten seconds has passed since the last page visit.
	</div>
	<div class="bg-zinc-900/60 rounded-md p-6 shadow-md  shadow-zinc-700/30">
		<div class="mb-2 text-sm uppercase text-white/60">Current Date:</div>
		<div class="text-2xl">
			{data.generatedAt}
		</div>
	</div>
</div>
