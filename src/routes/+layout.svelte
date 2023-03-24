<script>
	import '../app.css';
	import Nav from '$lib/Nav.svelte';
	import Header from '$lib/Header.svelte';
	import Footer from '$lib/Footer.svelte';
</script>

<div class="px-8 lg:px-0 h-screen flex flex-col justify-between">
	<Header />
	<div class="flex-grow w-full max-w-4xl mx-auto flex flex-col md:flex-row">
		<Nav />
		<div class="md:ml-12">
			<slot />
		</div>
	</div>
	<Footer />
</div>
