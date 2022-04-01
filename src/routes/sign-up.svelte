<script>
	let passwordType = true;
</script>

<svelte:head>
	<title>Sign Up</title>
</svelte:head>

<section class="lg:grid grid-cols-2 h-screen" id="auth">
	<div class="pt-16 pb-16 px-10 lg:px-20">
		<a href="/" class="font-bold text-xl" aria-label="Fiber's logo">Fiber</a>
		<h1 class="font-bold text-3xl mt-10 mb-5">Create your Fiber account</h1>
		<div>
			<form>
				<div class="mb-4">
					<label for="name" class="inline-block mb-2 font-bold">Your Name</label>
					<input
						type="text"
						class="border border-gray-300 p-3 w-full rounded-md"
						name="name"
						id="name"
						placeholder="John Doe"
					/>
				</div>
				<div class="mb-4">
					<label for="email" class="inline-block mb-2 font-bold">Email</label>
					<input
						type="text"
						class="border border-gray-300 p-3 w-full rounded-md"
						name="email"
						id="email"
						placeholder="john@example.com"
					/>
				</div>
				<div class="mb-8">
					<label for="password" class="inline-block mb-2 font-bold">Password</label>
					<div
						class="flex justify-between items-center focus-within:outline focus-within:outline-2 border border-gray-300 p-3 rounded-md"
					>
						<input
							type={`${passwordType ? 'password' : 'text'}`}
							class="w-full mr-4 outline-none"
							name="password"
							id="password"
							placeholder="At least 8 characters"
						/>
						<button type="button" on:click={() => (passwordType = !passwordType)}>
							<img src="/Assets/hide password.svg" alt="Hide/Show Password Toggle" />
						</button>
					</div>
				</div>
				<div class="mb-6">
					<input type="checkbox" class="mr-2" name="tnc" id="tnc" />
					<label for="tnc"
						>By creating an account on Fiber, you agree to the <a
							href="/"
							class="font-bold text-violet-blue border-b-2 border-b-violet-blue"
							>Terms & Conditions</a
						>.</label
					>
				</div>
				<button type="submit" class="p-4 w-full bg-violet-blue rounded-md text-white font-bold"
					>Create Fiber Account</button
				>
				<p class="mt-3 text-center">
					Already have an account? <a href="/" class="text-violet-blue">Sign In</a>
				</p>
			</form>
		</div>
	</div>
	<div class="bg-violet-blue hidden lg:grid place-content-center px-20 text-white text-center">
		<img src="/Assets/Sign Up Image.png" class="mb-6" alt="Illustration" />
		<h2 class="font-bold text-3xl mb-3">Unparalled Templates</h2>
		<p class="text-gray-200">
			Crafted by a team of professional designers, our templates are eunparalleled in the market.
		</p>
		<div class="flex justify-center mt-5">
			<button class="p-1.5 bg-white mr-2 rounded-full w-2" id="dot" />
			{#each Array(3) as _}
				<button class="p-1.5 bg-purple-mimosa mr-2 rounded-full w-2" id="dot" />
			{/each}
		</div>
	</div>
</section>
