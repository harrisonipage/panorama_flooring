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


{#if up}
<button on:click={showMenu} class="fixed top-2 right-5 h-fit w-fit z-[1000] hidden active:scale-95" in:fly={{ x: 100, duration: 400 }} out:fly={{ x: 100, duration: 400 }}>
	<span>
		<svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24"><rect x="0" y="0" width="24" height="24" fill="none" stroke="none" /><path fill="currentColor" d="M3 6h18v2H3V6m0 5h18v2H3v-2m0 5h18v2H3v-2Z"/></svg>
	</span>
</button>

{/if}
<div class="w-full h-16 fixed top-0 z-[1000] md:hidden bg-[#091426] border-b-gray-300 border-b disable-dbl-tap-zoom" >
	<a href="/" class="fixed top-2 left-5"><img src="/logo.png" alt="logo" class="h-10"/></a>

	<button on:click={showMobileMenu} class="fixed top-2 right-5 h-fit w-fit z-[1000] md:hidden">
		<span>
			<svg class="text-white" xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24"><rect x="0" y="0" width="24" height="24" fill="none" stroke="none" /><path fill="currentColor" d="M3 6h18v2H3V6m0 5h18v2H3v-2m0 5h18v2H3v-2Z"/></svg>
		</span>
	</button>
</div>
<main class="dark:text-white">
	<div id='nav' class="fixed top-0 w-screen h-[4.5rem] z-[999] overflow-x-clip border-b-gray-300 border-b duration-200 hidden md:block " in:fly={{ y: -100, duration: 400 }} out:fly={{ y: -100, duration: 400 }}>
		<AppBar gridColumns="grid-cols-3"  class="w-screen flex-col flex h-full justify-center text-white border-b-white" slotDefault="flex justify-center place-items-center" background="dark:bg-black bg-[#0a1629]" slotTrail="flex justify-end">
			<svelte:fragment slot="lead">
				<a href="/"><img src="/logo.png" alt="logo" class="md:h-[3rem]"/></a>
			</svelte:fragment>
			<svelte:fragment>
				<nav class="w-full p-4 text-lg overflow-x-hidden hidden md:flex text-white">
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
<div class="flex min-fit place-items-center flex-col p-5 md:p-10 py-20 justify-center gap-10 bg-[#091426] text-white">
	<div class="w-full h-full flex flex-col justify-evenly gap-20 place-items-center">
		<div class="text-4xl uppercase underline-offset-[15px] hover:text-gray-400 duration-150 underline"><a href="mailto:admin@panoramaflooring.com.au ?subject=Inquiry Panorama Flooring" class="flex-row flex gap-2"><span>Get In Touch</span> <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M13 19c0-3.31 2.69-6 6-6c1.1 0 2.12.3 3 .81V6a2 2 0 0 0-2-2H4c-1.11 0-2 .89-2 2v12a2 2 0 0 0 2 2h9.09c-.05-.33-.09-.66-.09-1M4 8V6l8 5l8-5v2l-8 5zm16 14v-2h-4v-2h4v-2l3 3z"/></svg></a></div>
		<form class="flex flex-col w-full gap-5 dark:text-white text-white hidden" action="https://api.staticforms.xyz/submitz" method="post">
			<input type="hidden" name="accessKey" value="e06e357f-f13e-4ae5-837a-f4caef655c72">
			<input type="text" name="honeypot" style="display: none;">
			<div class="flex flex-row w-full gap-5">			
				<input class="w-full border  border-l-0 border-r-0 border-t-0 placeholder:text-gray-100 focus:ring-0 focus:outline-none bg-gray-700 bg-opacity-50 rounded-t-lg" type="text" placeholder="Your Name" name="name" required/>
				<input class="w-full  border  border-l-0 border-r-0 border-t-0  placeholder:text-gray-100 focus:ring-0 bg-gray-700 bg-opacity-50 rounded-t-lg" type="text" placeholder="Your Number" name="phone" required/>
			</div>
			<input class="w-full  border border-l-0 border-r-0 border-t-0 placeholder:text-gray-100 focus:ring-0 bg-gray-700 bg-opacity-50 rounded-t-lg" type="text" placeholder="Your Email" name="email" required />
			<textarea class="resize-none border-t-0 border-r-0 border-l-0 placeholder:text-gray-100 focus:ring-0 bg-gray-700 bg-opacity-50 rounded-t-lg"  rows="4" name="message" placeholder="Tell us about your project" required/>
			<input type="hidden" name="redirectTo" value="https://panoramaflooring.com.au"> <!-- Optional -->
			<div class="g-recaptcha" data-sitekey="6LfjrOIpAAAAAGvwNO-FgY2j1eWhLMNy2Hk79-Gm"  data-callback="enableBtn"></div>
			<br/>

		</form>
	</div>
	<div class="h-full w-full md:w-1/2  flex justify-center place-items-center leading-loose text-lg font-light place-self-center text-center">
		<p>
			We believe communication is key when it comes to delivering the right commercial floor
			preparation service. It all starts here. If you have any questions about the flooring products
			or services we provide, you can contact us today for a FREE Quote.
		</p>
	</div>
</div>


<div class="h-fit bg-[#091426] border-t border-t-gray-800 flex flex-col p-10  gap-10 text-white">
	<div class="w-full h-full flex md:flex-row flex-col md:justify-between justify-center place-items-center gap-10">
		<a href="/"><img src="/logo.png" alt="logo" class="md:h-[3rem]"/></a>
		<div class="flex flex-row gap-2">
			<a href="https://instagram.com/panoramaflooring?igshid=OGQ5ZDc2ODk2ZA==">
				<span>
					<svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 24 24"><path fill="currentColor" d="M17.34 5.46a1.2 1.2 0 1 0 1.2 1.2a1.2 1.2 0 0 0-1.2-1.2Zm4.6 2.42a7.59 7.59 0 0 0-.46-2.43a4.94 4.94 0 0 0-1.16-1.77a4.7 4.7 0 0 0-1.77-1.15a7.3 7.3 0 0 0-2.43-.47C15.06 2 14.72 2 12 2s-3.06 0-4.12.06a7.3 7.3 0 0 0-2.43.47a4.78 4.78 0 0 0-1.77 1.15a4.7 4.7 0 0 0-1.15 1.77a7.3 7.3 0 0 0-.47 2.43C2 8.94 2 9.28 2 12s0 3.06.06 4.12a7.3 7.3 0 0 0 .47 2.43a4.7 4.7 0 0 0 1.15 1.77a4.78 4.78 0 0 0 1.77 1.15a7.3 7.3 0 0 0 2.43.47C8.94 22 9.28 22 12 22s3.06 0 4.12-.06a7.3 7.3 0 0 0 2.43-.47a4.7 4.7 0 0 0 1.77-1.15a4.85 4.85 0 0 0 1.16-1.77a7.59 7.59 0 0 0 .46-2.43c0-1.06.06-1.4.06-4.12s0-3.06-.06-4.12ZM20.14 16a5.61 5.61 0 0 1-.34 1.86a3.06 3.06 0 0 1-.75 1.15a3.19 3.19 0 0 1-1.15.75a5.61 5.61 0 0 1-1.86.34c-1 .05-1.37.06-4 .06s-3 0-4-.06a5.73 5.73 0 0 1-1.94-.3a3.27 3.27 0 0 1-1.1-.75a3 3 0 0 1-.74-1.15a5.54 5.54 0 0 1-.4-1.9c0-1-.06-1.37-.06-4s0-3 .06-4a5.54 5.54 0 0 1 .35-1.9A3 3 0 0 1 5 5a3.14 3.14 0 0 1 1.1-.8A5.73 5.73 0 0 1 8 3.86c1 0 1.37-.06 4-.06s3 0 4 .06a5.61 5.61 0 0 1 1.86.34a3.06 3.06 0 0 1 1.19.8a3.06 3.06 0 0 1 .75 1.1a5.61 5.61 0 0 1 .34 1.9c.05 1 .06 1.37.06 4s-.01 3-.06 4ZM12 6.87A5.13 5.13 0 1 0 17.14 12A5.12 5.12 0 0 0 12 6.87Zm0 8.46A3.33 3.33 0 1 1 15.33 12A3.33 3.33 0 0 1 12 15.33Z"/></svg>
				</span>
			</a>
		</div>
	</div>
	<div class="justify-center place-items-center flex text-center">
		<h1>© 2024, Panorama Flooring</h1>
	</div>
</div>
</main>
<svelte:window bind:scrollY={y} on:scroll={scrollhandle}/>


<style>
	.disable-dbl-tap-zoom {
  touch-action: manipulation;
}
</style>