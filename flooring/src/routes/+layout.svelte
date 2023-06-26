<script lang='ts'>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import type { DrawerSettings } from '@skeletonlabs/skeleton';
	import {fly} from 'svelte/transition'

	let y = 0
</script>

<Drawer position="top" rounded="none" bgDrawer="bg-white" height="h-fit">
	<div class="h-[5rem] w-full">

	</div>
	<nav class="text-black w-full flex p-4 text-lg overflow-x-hidden no-underline">
		<ul class="flex flex-col gap-8 font-semibold uppercase no-underline">
			<a class="hover:text-yellow-400 no-underline" href="/"><li class="no-underline">home</li></a>
			<a href="/about"><li>about us</li></a>
			<a href="/projects"><li>projects</li></a>
			<a href="/contact"><li>contact</li></a>
		</ul>
	</nav>
</Drawer>
<!-- App Shell -->
			{#if (y>3)}
			<div  class="fixed top-0 w-screen h-[4.5rem] underline border-b-gray-200 border z-[999] overflow-x-clip hidden md:block" in:fly={{ y: -100, duration: 400 }} out:fly={{ y: -100, duration: 400 }}>
				<AppBar gridColumns="grid-cols-3"  class="w-screen flex-col flex h-full justify-center text-black" background="bg-white">
					<svelte:fragment slot="lead">
						<img src="/logo.png" alt="logo" class="invert h-[4rem]" />
					</svelte:fragment>
					<svelte:fragment>
						<nav class="text-black w-full flex p-4 text-lg overflow-x-hidden no-underline">
							<ul class="flex flex-row gap-8 font-semibold uppercase no-underline">
								<a class="hover:text-yellow-400 no-underline" href="/"><li>home</li></a>
								<a href="/about"><li>about us</li></a>
								<a href="/projects"><li>projects</li></a>
								<a href="/contact"><li>contact</li></a>
							</ul>
						</nav>
					</svelte:fragment>
				</AppBar>
			</div>
			{/if}
			<div  class="fixed top-0 w-screen h-[5rem] underline border-b-gray-200 border z-[999] overflow-x-clip md:hidden">
				<AppBar class="w-screen flex-col flex h-full justify-center text-black" background="bg-white">
					<svelte:fragment slot="lead">
						<strong class="text-xl uppercase no-underline">LOGO</strong>
					</svelte:fragment>
					<svelte:fragment slot="trail">
						<button on:click={()=>(drawerStore.open())}>
							<span> 
								<svg viewBox="0 0 100 80" class="fill-black w-6 h-6"> 
									<rect width="100" height="20" /> 
									<rect y="30" width="100" height="20" />
									<rect y="60" width="100" height="20" /> 
								</svg> 
							</span>
						</button>
					</svelte:fragment>
				</AppBar>
			</div>

	<!-- Page Route Content -->
	<slot />
<div class="h-72 bg-slate-200 flex flex-col p-10 text-black">
	<div class="w-full h-full flex md:flex-row flex-col md:justify-between justify-center place-items-center gap-5">
		<h1>LOGO</h1>
		<h2>Socials</h2>
	</div>
	<div class="justify-center place-items-center flex text-center">
		<h1>© 2023, Panorama Flooring <span class="italic">designed by <a href="/">hp</a></span></h1>

	</div>

</div>

<svelte:window bind:scrollY={y}/>
