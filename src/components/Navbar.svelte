<script>
	import Container from './Container.svelte';

	let hasOpen = false;
	let offset;
</script>

<svelte:window bind:scrollY={offset} />

<nav
	class={`py-6 fixed top-0 w-full ${
		hasOpen || offset >= 75 ? 'bg-white backdrop-blur-sm bg-opacity-60' : 'bg-transparent'
	}`}
>
	<Container classes="block lg:flex justify-between items-center">
		<div class="flex justify-between items-center">
			<a href="/" aria-label="Logo" class="font-bold">Fiber</a>
			<button class="block lg:hidden" on:click={() => (hasOpen = !hasOpen)}>
				<img src="/Assets/Hamburger Menu.svg" alt="Hamburger Menu" />
			</button>
		</div>
		<ul class={`${hasOpen ? 'block' : 'hidden'} lg:flex mt-8 lg:mt-0`}>
			<li class="mr-8 mb-4 lg:mb-0">
				<a href="/" aria-label="Navigation link">Community</a>
			</li>
			<li class="mr-8 mb-4 lg:mb-0">
				<a href="/" aria-label="Navigation link">Pricing</a>
			</li>
			<li class="mb-4 lg:mb-0">
				<a href="/" aria-label="Navigation link">Features</a>
			</li>
		</ul>
		<ul class={`${hasOpen ? 'block' : 'hidden'} lg:flex`}>
			<li class="mr-8 mb-4 lg:mb-0">
				<a href="/" class="font-bold" aria-label="Navigation link">Sign In</a>
			</li>
			<li>
				<a
					href="/sign-up"
					class="bg-violet-blue inline-block lg:inline lg:mt-0 font-bold py-3 px-5 text-white rounded-md"
					role="button">Sign Up</a
				>
			</li>
		</ul>
	</Container>
</nav>
