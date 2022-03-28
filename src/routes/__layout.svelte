<script>
	import '../../static/css/tailwind.css';
	import Navbar from '../components/Navbar.svelte';
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<main class="font-inter">
	<Navbar />
	<slot />
</main>
