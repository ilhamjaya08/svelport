<script>
	import '../app.postcss';
	// @ts-ignore
	import { Avatar, Navbar, NavBrand, NavLi, NavUl, NavHamburger, DarkMode } from 'flowbite-svelte';
	// @ts-ignore
	import { onMount } from 'svelte';
	import Foot from '$lib/components/Foot.svelte';
	import NavButton from '$lib/components/atoms/NavButton.svelte';
	var hasIconLoaded = false;
	onMount(() => {
		hasIconLoaded = true;
	});
</script>

<html lang="en">
	<head>
		<title>ilhamjaya08 | Portfolio</title>
		<link
			rel="stylesheet"
			href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
			integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw=="
			crossorigin="anonymous"
			referrerpolicy="no-referrer"
		/>
	</head>
	<body class="dark:bg-gray-900 overflow-hidden before:absolute before:w-12 before:h-12 before:content[''] before:right-0 before:bg-violet-500 before:rounded-full before:blur-lg before:[box-shadow:-60px_20px_10px_10px_#F9B0B9]">
		<Navbar class="md:px-60 py-3 px-6 md:py-6" let:hidden let:toggle>
			<div class="nav flex justify-between w-full md:w-auto md:block">
				
				<NavBrand href="/">
					{#if hasIconLoaded}
						<div class="container">
							<Avatar
								src="https://avatars.githubusercontent.com/u/141555404?v=4"
								class="avatar mr-3 hover:rotate-360 transition duration-1000 ease-in-out h-12 w-12 md:h-16 md:w-16"
								alt=""
							/>
						</div>
					{:else}
						<div
							class="animate-spin rounded-full h-12 w-12 md:h-16 md:w-16 border-t-2 border-b-2 border-gray-900 dark:border-gray-100"
						/>
					{/if}
				</NavBrand>
				<div class="end-nav flex list-none">
					<NavHamburger on:click={toggle} />
				</div>
			</div>

			<NavUl
				ulClass="text-xl md:text-2xl flex space-x-8 space-y-4 md:space-y-0 pb-4 justify-center items-center flex-col my-3 md:m-0 md:flex-row"
				{hidden}
				activeClass="text-latte-blue dark:text-ctp-mauve underline underline-offset-8 decoration-2 font-semibold"
				nonActiveClass="hover:text-latte-lavender dark:hover:text-ctp-mauve"
			>
				<div class="hidden md:block"><NavLi><DarkMode size="lg" initialTheme="dark" /></NavLi></div>
				<NavButton href="/">Home</NavButton>
				<NavButton href="/about">About</NavButton>
				<NavButton href="/works">Works</NavButton>
				<NavButton href="/contact">Contact</NavButton>
			</NavUl>
		</Navbar>
		<div
           id="par" class="absolute blur duration-500  hover:blur-none w-72 h-72 rounded-full hover:translate-x-12 hover:translate-y-12 bg-violet-200 dark:bg-sky-800 bg-opacity-40 left-1 "
        ></div>
		<div
           id="parr" class="absolute blur duration-500  animate-[ping_5s_linear_infinite] hover:blur-none w-12 h-12 rounded-full hover:translate-x-12 hover:translate-y-2 bg-opacity-75 bg-indigo-500 right-12 bottom-12"
        ></div>
        <div
           id="parrr" class="absolute blur duration-500 hover:blur-none w-36 h-36 rounded-full bg-opacity-50 hover:translate-x-12 hover:-translate-y-12 bg-indigo-200 right-[38rem] "
        ></div>
        <div
           id="parrrr" class="absolute blur duration-500 hover:blur-none w-24 h-24 bg-sky-200 bg-opacity-50 dark:bg-sky-300 rounded-full left-24 -bottom-10 hover:-translate-x-12"
        ></div>

		<slot />

		<Foot />
	</body>
</html>
