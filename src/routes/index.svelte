<script>
	import Container from '../components/Container.svelte';
	import { MetaTags } from 'svelte-meta-tags';
	import { reviews } from '../data';
	import Navbar from '../components/Navbar.svelte';
</script>

<MetaTags title="Fiber" description="Create your portfolio in minutes with Fiber" />

<Navbar />
<section class="md:h-screen grid items-center mb-16">
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
<section class="mb-16" id="features">
	<Container>
		<p class="text-violet-blue font-bold mb-2">Why Fiber?</p>
		<h2 class="text-4xl font-bold mb-10">A good portfolio means good<br />employability.</h2>
		<div class="grid md:grid-cols-3 gap-12">
			<div>
				<img src="/Assets/time.svg" alt="Time" />
				<h3 class="font-bold my-3">Build in minutes</h3>
				<p class="text-gray-600">
					With a selection of premade templates, you can build out a portfolio in less than 10
					minutes.
				</p>
			</div>
			<div>
				<img src="/Assets/code.svg" alt="Time" />
				<h3 class="font-bold my-3">Build in minutes</h3>
				<p class="text-gray-600">
					Customize your personal portfolio even more with the ability to add your own custom CSS
					styles.
				</p>
			</div>
			<div>
				<img src="/Assets/allSizes.svg" alt="Time" />
				<h3 class="font-bold my-3">Build in minutes</h3>
				<p class="text-gray-600">
					All Fiber templates are fully responsive to ensure the experience is seemless across all
					devices.
				</p>
			</div>
		</div>
	</Container>
</section>
<section class="mb-16" id="offer">
	<Container>
		<div class="bg-violet-blue grid md:grid-cols-2 gap-10 items-center px-10 rounded-lg pt-10">
			<div class="text-white md:pb-10">
				<h2 class="font-bold text-4xl">Diversify your portfolio.</h2>
				<p class="my-4">
					Create an even more impressive portfolio by creating case studies for your projects.
					Simply follow our step-by-step guide.
				</p>
				<a
					href="/sign-up"
					class="inline-block bg-white text-violet-blue p-4 mr-5 mb-5 md:mb-0 rounded-md font-bold w-full md:w-auto"
					role="button">Start Free Trial</a
				>
			</div>
			<img src="/Assets/Page Image.png" class="md:self-end" alt="Page" />
		</div>
	</Container>
</section>
<section class="mb-16">
	<Container classes="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
		{#each reviews as review}
			<div class="border border-gray-300 p-8 rounded-lg h-full">
				<div class="flex items-center">
					<img src={`/Assets/${review.photo}.svg`} class="mr-3" alt="Sarah Andrews" />
					<div>
						<a href="/" class="text-violet-blue font-bold" aria-label="Sarah Andrews's profile"
							>{review.name}</a
						>
						<p>${review.revenue}k in revenue</p>
					</div>
				</div>
				<p class="my-5">{review.text}</p>
				<a
					href="/"
					class="font-bold text-violet-blue border border-gray-300 block rounded-md text-center py-3"
					role="button">View Sarah's Portfolio</a
				>
			</div>
		{/each}
	</Container>
</section>
<footer class="py-10 bg-gray-100">
	<Container>
		<div class="md:grid grid-cols-5 gap-10">
			<div class="mb-5 md:mb-0">
				<a href="/" class="font-bold inline-block mb-3" aria-label="Logo">Fiber</a>
				<p class="text-gray-600">
					With Fiber, you can setup your own personal portfolio in minutes with dozens of premade,
					beautiful templates.
				</p>
			</div>
			<ul class="mb-5 md:mb-0">
				<p class="mb-3 font-bold">Sitemap</p>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Homepage">Homepage</a>
				</li>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Pricing">Pricing</a>
				</li>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Testimonials">Testimonials</a>
				</li>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Features">Features</a>
				</li>
			</ul>
			<ul class="mb-5 md:mb-0">
				<p class="mb-3 font-bold">Resources</p>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Support">Support</a>
				</li>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Contact">Contact</a>
				</li>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="FAQ">FAQ</a>
				</li>
			</ul>
			<ul class="mb-5 md:mb-0">
				<p class="mb-3 font-bold">Company</p>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="About">About</a>
				</li>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Customers">Customers</a>
				</li>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Blog">Blog</a>
				</li>
			</ul>
			<ul class="mb-5 md:mb-0">
				<p class="mb-3 font-bold">Portfolios</p>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Sarah Andrews">Sarah Andrews</a>
				</li>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Matthew Higgins">Matthew Higgins</a>
				</li>
				<li class="mb-3">
					<a href="/" class="text-gray-600" aria-label="Janice Dave">Janice Dave</a>
				</li>
			</ul>
		</div>
		<p class="text-gray-600 mt-10">
			Made with <i class="fas fa-fw fa-heart" /> in the Netherlands.
		</p>
	</Container>
</footer>
