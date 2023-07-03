<script lang="ts">
	// Your selected Skeleton theme:
	import '@skeletonlabs/skeleton/themes/theme-skeleton.css';

	// This contains the bulk of Skeletons required styles:
	import '@skeletonlabs/skeleton/styles/skeleton.css';

	// Finally, your application's global stylesheet (sometimes labeled 'app.css')
	import '../app.postcss';

	import { AppBar } from '@skeletonlabs/skeleton';
	import { Drawer, drawerStore, LightSwitch } from '@skeletonlabs/skeleton';
	import {fly} from 'svelte/transition'

	let y = 0
	let oldScroll = 0
	let up = true
	let open = false
	let showing = false

	
	function scrollhandle(){
		if (showing || y<=0 ){
			up = true
			return
		}
		if (open){
			up = true
			return
		}
		if( oldScroll > y){
			oldScroll = y
			up = true
		}
		else{
			oldScroll = y
			up = false
		}
	}

	function showMenu() {
		console.log('here')
		let nav = document.getElementById('nav')
		if (nav){
			nav.classList.toggle('-translate-y-full')
			showing = !showing
		}
	}
	function showMobileMenu(){
		if (open){
			drawerStore.close()
			open = false
		}
		else{
			drawerStore.open()
			open = true
		}
	}
</script>
<Drawer position="right" rounded="none" bgDrawer="dark:bg-black bg-white" height="h-full" width="w-full" bgBackdrop="bg-none">
	<nav class="w-full flex p-4 text-lg focus:ring-0 h-full justify-center">
		<ul class="flex flex-col gap-8 font-medium uppercase tracking-wide justify-center place-items-center">
			<li><a class="focus:ring-0" on:click={()=>drawerStore.close()}  href="/">home</a></li>
			<li><a on:click={()=>drawerStore.close()}  href="/about">about us</a></li>
			<li><a on:click={()=>drawerStore.close()}  href="/projects">projects</a></li>
			<li><a on:click={()=>drawerStore.close()}  href="/contact">contact</a></li>
		</ul>
	</nav>
</Drawer>
<div class="fixed top-5 right-20 z-[1000000]">
	<LightSwitch></LightSwitch>
</div>

{#if up}
<button on:click={showMenu} class="fixed top-2 right-5 h-fit w-fit z-[1000] hidden md:block active:scale-95" in:fly={{ x: 100, duration: 400 }} out:fly={{ x: 100, duration: 400 }}>
	<span>
		<svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24"><rect x="0" y="0" width="24" height="24" fill="none" stroke="none" /><path fill="currentColor" d="M3 6h18v2H3V6m0 5h18v2H3v-2m0 5h18v2H3v-2Z"/></svg>
	</span>
</button>
<button on:click={showMobileMenu} class="fixed top-2 right-5 h-fit w-fit z-[1000] md:hidden" in:fly={{ x: 100, duration: 400 }} out:fly={{ x: 100, duration: 400 }}>
	<span>
		<svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24"><rect x="0" y="0" width="24" height="24" fill="none" stroke="none" /><path fill="currentColor" d="M3 6h18v2H3V6m0 5h18v2H3v-2m0 5h18v2H3v-2Z"/></svg>
	</span>
</button>
{/if}
<main class="dark:text-white text-black dark:bg-black">
	<div id='nav' class="fixed top-0 w-screen h-[4.5rem] z-[999] overflow-x-clip border-b-gray-600 border-b duration-200 hidden md:block -translate-y-full" in:fly={{ y: -100, duration: 400 }} out:fly={{ y: -100, duration: 400 }}>
		<AppBar gridColumns="grid-cols-3"  class="w-screen flex-col flex h-full justify-center text-white border-b-white" slotDefault="flex justify-center place-items-center" background="dark:bg-black bg-surface-100" slotTrail="flex justify-end">
			<svelte:fragment slot="lead">
				<a href="/"><img src="/logo.png" alt="logo" class="md:h-[3rem] dark:invert-0 invert"/></a>
			</svelte:fragment>
			<svelte:fragment>
				<nav class="w-full p-4 text-lg overflow-x-hidden hidden md:flex dark:text-white text-black">
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
	<!---
{:else}
<div  class="fixed top-0 w-screen h-[4.5rem] border-b-gray-600 z-[999] overflow-x-clip border-b" out:fly={{ y: -100, duration: 400 }}>
	<AppBar gridColumns="grid-cols-3"  class="w-screen flex-col flex h-full justify-center text-white" slotDefault="flex justify-center place-items-center" background="bg-black" slotTrail="flex justify-end">
		<svelte:fragment slot="lead">
			<a href="/"><img src="/logo.png" alt="logo" class="md:h-[3rem]"/></a>
		</svelte:fragment>
		<svelte:fragment>
			<nav class="text-white w-full p-4 text-lg overflow-x-hidden hidden md:flex">
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
-->
<slot />

<div class="h-fit dark:bg-black border-t border-t-gray-800 flex flex-col p-10  gap-10">
	<div class="w-full h-full flex md:flex-row flex-col md:justify-between justify-center place-items-center gap-10">
		<a href="/"><img src="/logo.png" alt="logo" class="md:h-[3rem] dark:invert-0 invert"/></a>
		<div class="flex flex-row gap-2">
			<span>
				<svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24"><path fill="currentColor" d="M17.34 5.46a1.2 1.2 0 1 0 1.2 1.2a1.2 1.2 0 0 0-1.2-1.2Zm4.6 2.42a7.59 7.59 0 0 0-.46-2.43a4.94 4.94 0 0 0-1.16-1.77a4.7 4.7 0 0 0-1.77-1.15a7.3 7.3 0 0 0-2.43-.47C15.06 2 14.72 2 12 2s-3.06 0-4.12.06a7.3 7.3 0 0 0-2.43.47a4.78 4.78 0 0 0-1.77 1.15a4.7 4.7 0 0 0-1.15 1.77a7.3 7.3 0 0 0-.47 2.43C2 8.94 2 9.28 2 12s0 3.06.06 4.12a7.3 7.3 0 0 0 .47 2.43a4.7 4.7 0 0 0 1.15 1.77a4.78 4.78 0 0 0 1.77 1.15a7.3 7.3 0 0 0 2.43.47C8.94 22 9.28 22 12 22s3.06 0 4.12-.06a7.3 7.3 0 0 0 2.43-.47a4.7 4.7 0 0 0 1.77-1.15a4.85 4.85 0 0 0 1.16-1.77a7.59 7.59 0 0 0 .46-2.43c0-1.06.06-1.4.06-4.12s0-3.06-.06-4.12ZM20.14 16a5.61 5.61 0 0 1-.34 1.86a3.06 3.06 0 0 1-.75 1.15a3.19 3.19 0 0 1-1.15.75a5.61 5.61 0 0 1-1.86.34c-1 .05-1.37.06-4 .06s-3 0-4-.06a5.73 5.73 0 0 1-1.94-.3a3.27 3.27 0 0 1-1.1-.75a3 3 0 0 1-.74-1.15a5.54 5.54 0 0 1-.4-1.9c0-1-.06-1.37-.06-4s0-3 .06-4a5.54 5.54 0 0 1 .35-1.9A3 3 0 0 1 5 5a3.14 3.14 0 0 1 1.1-.8A5.73 5.73 0 0 1 8 3.86c1 0 1.37-.06 4-.06s3 0 4 .06a5.61 5.61 0 0 1 1.86.34a3.06 3.06 0 0 1 1.19.8a3.06 3.06 0 0 1 .75 1.1a5.61 5.61 0 0 1 .34 1.9c.05 1 .06 1.37.06 4s-.01 3-.06 4ZM12 6.87A5.13 5.13 0 1 0 17.14 12A5.12 5.12 0 0 0 12 6.87Zm0 8.46A3.33 3.33 0 1 1 15.33 12A3.33 3.33 0 0 1 12 15.33Z"/></svg>
			</span>
			<span>
				<svg xmlns="http://www.w3.org/2000/svg" width="45" height="45" viewBox="0 0 16 16"><path fill="currentColor" d="M16 8.049c0-4.446-3.582-8.05-8-8.05C3.58 0-.002 3.603-.002 8.05c0 4.017 2.926 7.347 6.75 7.951v-5.625h-2.03V8.05H6.75V6.275c0-2.017 1.195-3.131 3.022-3.131c.876 0 1.791.157 1.791.157v1.98h-1.009c-.993 0-1.303.621-1.303 1.258v1.51h2.218l-.354 2.326H9.25V16c3.824-.604 6.75-3.934 6.75-7.951z"/></svg>
			</span>
		</div>
	</div>
	<div class="justify-center place-items-center flex text-center">
		<h1>© 2023, Panorama Flooring <span class="italic">designed by <a href="/">hp</a></span></h1>
	</div>
</div>
</main>
<svelte:window bind:scrollY={y} on:scroll={scrollhandle}/>
