<script>
	import '../app.css';
	import Nav from '../lib/Nav.svelte';
	import Header from '../lib/Header.svelte';
	import Footer from '../lib/Footer.svelte';
</script>

<div class="h-screen flex flex-col justify-between">
	<Header />
	<div class="flex-grow w-full max-w-4xl mx-auto flex ">
		<Nav />
		<div class="ml-12">
			<slot />
		</div>
	</div>
	<Footer />
</div>
