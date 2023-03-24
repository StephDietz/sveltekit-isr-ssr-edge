<script>
	import { page } from '$app/stores';

	$: path = $page.url.pathname;
	let tabs = [
		{ name: 'Home', path: '/' },
		{ name: 'SSR', path: '/ssr' },
		{ name: 'Edge', path: '/edge' },
		{ name: 'ISR', path: '/isr' }
	];
</script>

<div>
	<nav class="flex md:flex-col justify-between md:justify-start md:space-x-0 space-x-2">
		{#each tabs as tab, i (i)}
			<a
				href={tab.path}
				class={`${
					path === tab.path ? 'bg-zinc-900' : 'bg-zinc-900/60'
				} rounded-md p-2 w-1/4 md:w-32 mb-6 shadow-md  shadow-zinc-700/30 text-center`}
			>
				{tab.name}
			</a>
		{/each}
	</nav>
</div>
