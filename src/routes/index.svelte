<script>
	import Container from '../components/Container.svelte';
	import { MetaTags } from 'svelte-meta-tags';
</script>

<MetaTags title="Fiber" description="Create your portfolio in minutes with Fiber" />

<section class="h-screen grid items-center">
	<Container classes="grid md:grid-cols-2 items-center">
		<div class="order-2 md:order-1">
			<div class="mb-4 hidden md:block">
				{#each Array(5) as _}
					<img src="/Assets/star.svg" class="inline mr-2" alt="Star" />
				{/each}
				<p class="inline align-middle">Rated 4.8/5 (243 reviews)</p>
			</div>
			<h1 class="font-bold text-5xl leading-snug mb-1">Create your portfolio in minutes.</h1>
			<p class="text-gray-700 mb-5">
				With Fiber, you can setup your own personal portfolio in minutes with dozens of premade,
				beautiful templates.
			</p>
			<div class="text-center md:text-left">
				<a
					href="/sign-up"
					class="inline-block bg-violet-blue text-white p-4 mr-5 mb-5 md:mb-0 rounded-md font-bold w-full md:w-auto"
					role="button">Start Free Trial</a
				>
				<a href="/" class="font-bold text-violet-blue border-b-2 border-b-violet-blue"
					>View Examples</a
				>
			</div>
			<ul class="block md:flex mt-7 md:mt-5 text-gray-600">
				<li class="flex items-center mr-6 mb-4 md:mb-0">
					<img src="/Assets/Checkmark.svg" class="mr-2" alt="Checkmark" />
					<p>No Credit Card Required</p>
				</li>
				<li class="flex items-center">
					<img src="/Assets/Checkmark.svg" class="mr-2" alt="Checkmark" />
					<p>10 Free Templates</p>
				</li>
			</ul>
		</div>
		<img
			src="/Assets/hero-Illustration.png"
			class="order-1 md:order-2 mb-6 lg:mb-0"
			alt="Hero Illustration"
		/>
	</Container>
</section>
