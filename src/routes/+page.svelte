<script>
	import { fade, blur, slide } from 'svelte/transition';
	import { quadInOut } from 'svelte/easing';
	import { onMount } from 'svelte';
	import CircularButton from '$lib/components/atoms/CircularButton.svelte';
	import { user } from '../data/Data';
	import Page from './contact/+page.svelte';
	import FormCards from '$lib/components/FormCards.svelte';
	let animate = false;

	const helloInDifferentLanguages = [
		'Student',
		'Junior Developer',
		'Software Engineer',
		'Cool Man'
	];

	let currentHello = helloInDifferentLanguages[0];
	let currentIndex = 0;

	// update the hello text with the next language
	function updateHelloText() {
		currentIndex = (currentIndex + 1) % helloInDifferentLanguages.length;
		currentHello = helloInDifferentLanguages[currentIndex];
	}
	onMount(() => {
		animate = true;
		setInterval(updateHelloText, 2000);
	});
</script>

<section class="pt-28 dark:bg-gray-900 mocha">
	{#if animate}
		<div
			class="py-8 px-4 mx-auto max-w-screen-xl text-center lg:py-16"
			transition:blur|local={{ duration: 500 }}
		>
			<div class="flex justify-center">
				
				<h1 class="mb-4 text-4xl py-2 font-bold md:text-6xl lg:text-8xl bg-clip-text text-transparent bg-gradient-to-r from-sky-300 via-pink-500 to-purple-700  sticky">
					{user.name}
				</h1>
			</div>

			<p
					class="mb-4 text-xl p-0 font-bold md:text-2xl lg:text-4xl dark:text-white flex flex-col-reverse"
				> 
					{#key currentHello}
						{#if currentHello}
							<span
								class="py-2 text-latte-blue dark:text-ctp-mauve text-center"
								transition:slide={{ duration: 1000, easing: quadInOut }}
								> {currentHello}! &nbsp
							</span>
						{/if}
					{/key}
			</p>
		</div>

		<div class="flex items-center justify-center" transition:fade|local={{ duration: 700 }}>
			<CircularButton size="md" href="/contact">👋 &nbsp;Explore this site</CircularButton>
		</div>
		<FormCards/>
	{/if}
	
</section>
