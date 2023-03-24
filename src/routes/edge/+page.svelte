<script>
	/** @type {import('./$types').PageData} */
	export let data;
</script>

<div>
	<div class="font-bold text-2xl mb-4">Edge Functions</div>
	<div class="opacity-80 mb-4">
		This page is returning the date from a SvelteKit page endpoint with edge configuration
		specified. This means that when deployed to Vercel, this endpoint will be turned into and edge
		function which enables you to deliver dynamic, personalized content with the lightweight Edge
		Runtime which is more performant and cost-effective than Serverless Functions. Edge Functions
		are deployed globally on an Edge Network, and can automatically execute in the region nearest to
		the user. Learn more about edge functions <a
			class="text-blue-400 hover:text-blue-400"
			href="https://vercel.com/docs/concepts/functions/edge-functions"
			target="_blank">here</a
		>.
	</div>
	<div class="opacity-80 mb-4">
		This page endpoint runs on the edge, and returns the current date and time. Notice each time you
		refresh the page, the endpoint runs again and the time is updated.
	</div>
	<div class="bg-zinc-900/60 rounded-md p-6 shadow-md mb-4 shadow-zinc-700/30">
		<div class="mb-2 text-sm uppercase text-white/60">Current Date:</div>
		<div class="text-2xl">
			{data.generatedAt}
		</div>
	</div>
</div>
