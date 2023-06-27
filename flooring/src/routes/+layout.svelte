<script lang="ts">
	// Your selected Skeleton theme:
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';

	// This contains the bulk of Skeletons required styles:
	import '@skeletonlabs/skeleton/styles/skeleton.css';

	// Finally, your application's global stylesheet (sometimes labeled 'app.css')
	import '../app.postcss';

	import { AppBar } from '@skeletonlabs/skeleton';
	import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import {fly} from 'svelte/transition'

	let y = 3
	export let data
</script>
<Drawer position="top" rounded="none" bgDrawer="bg-white" height="h-fit">
	<div class="h-[5rem] w-full">
	</div>
	<nav class="text-black w-full flex p-4 text-lg">
		<ul class="flex flex-col gap-8 font-medium uppercase tracking-wide">
			<li><a class="focus:ring-0" on:click={()=>drawerStore.close()}  href="/">home</a></li>
			<li><a on:click={()=>drawerStore.close()}  href="/about">about us</a></li>
			<li><a on:click={()=>drawerStore.close()}  href="/projects">projects</a></li>
			<li><a on:click={()=>drawerStore.close()}  href="/contact">contact</a></li>
		</ul>
	</nav>
</Drawer>

{#if (data.url === '/')}
	{#if (y>40)}	
	<div  class="fixed top-0 w-screen h-[4.5rem] underline border-b-gray-200 border z-[999] overflow-x-clip " in:fly={{ y: -100, duration: 400 }} out:fly={{ y: -100, duration: 400 }}>
		<AppBar gridColumns="grid-cols-3"  class="w-screen flex-col flex h-full justify-center text-black" slotDefault="flex justify-center place-items-center" background="bg-white" slotTrail="flex justify-end">
			<svelte:fragment slot="lead">
				<a href="/"><img src="/logo.png" alt="logo" class="invert md:h-[3rem]"/></a>
			</svelte:fragment>
			<svelte:fragment>
				<nav class="text-black w-full p-4 text-lg overflow-x-hidden hidden md:flex">
					<ul class="flex flex-row gap-8 uppercase w-full justify-between text-sm	 font-medium">
						<li><a href="/">home</a></li>
						<li><a href="/about">about</a></li>
						<li><a href="/projects">projects</a></li>
						<li><a href="/contact">contact</a></li>
					</ul>						
				</nav>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<button class="place-self-end md:hidden" on:click={() => drawerStore.open()}>
					<span>
						<svg xmlns="http://www.w3.org/2000/svg" width="35" height="35" viewBox="0 0 24 24"><rect x="0" y="0" width="24" height="24" fill="none" stroke="none" /><path fill="currentColor" d="M3 6h18v2H3V6m0 5h18v2H3v-2m0 5h18v2H3v-2Z"/></svg>
					</span>
				</button>
			</svelte:fragment>
		</AppBar>
	</div>
	{/if}
{:else}
<div  class="fixed top-0 w-screen h-[4.5rem] underline border-b-gray-200 border z-[999] overflow-x-clip " out:fly={{ y: -100, duration: 400 }}>
	<AppBar gridColumns="grid-cols-3"  class="w-screen flex-col flex h-full justify-center text-black" slotDefault="flex justify-center place-items-center" background="bg-white" slotTrail="flex justify-end">
		<svelte:fragment slot="lead">
			<a href="/"><img src="/logo.png" alt="logo" class="invert md:h-[3rem]"/></a>
		</svelte:fragment>
		<svelte:fragment>
			<nav class="text-black w-full p-4 text-lg overflow-x-hidden hidden md:flex">
				<ul class="flex flex-row gap-8 uppercase w-full justify-between text-sm	 font-medium">
					<li><a href="/">home</a></li>
					<li><a href="/about">about</a></li>
					<li><a href="/projects">projects</a></li>
					<li><a href="/contact">contact</a></li>
				</ul>						
			</nav>
		</svelte:fragment>
		<svelte:fragment slot="trail">
			<button class="place-self-end md:hidden" on:click={() => drawerStore.open()}>
				<span>
					<svg xmlns="http://www.w3.org/2000/svg" width="35" height="35" viewBox="0 0 24 24"><rect x="0" y="0" width="24" height="24" fill="none" stroke="none" /><path fill="currentColor" d="M3 6h18v2H3V6m0 5h18v2H3v-2m0 5h18v2H3v-2Z"/></svg>
				</span>
			</button>
		</svelte:fragment>
	</AppBar>
</div>
{/if}
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
