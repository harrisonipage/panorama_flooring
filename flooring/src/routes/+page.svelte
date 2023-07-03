<script>

	import { enhance } from "$app/forms";
	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';
</script>

<div class="h-fit w-full justify-center flex flex-col place-items-center dark:bg-black text-black dark:text-white gap-10 mb-20 md:space-y-20">
	<section id="hero" class="w-full h-screen justify-center place-items-center flex bg-fixed bg-cover bg-bottom dark:text-white p-10 flex-col gap-10">
		<h1 class="text-6xl md:text-9xl text-center font-bold">PANORAMA FLOORING</h1>
		<h1 class="text-3xl font-medium">Quality above all else</h1>
		<p class="min-w-96 max-w-screen-md text-center text-lg hidden md:block">We understand the importance of minimising delays on building projects. 
			This is why we are dedicated to providing a fast and efficient floor preparation 
			service done by qualified and insured professionals with minimal interruptions.
			</p>
		<div class="flex flex-col md:flex-row gap-5 md:gap-10 w-full justify-center cursor-pointer pointer-events-auto">
			<a class=" px-5 py-3 border-gray-400 dark:bg-white bg-black text-white dark:text-black w-full md:w-48 text-center active:scale-95 duration-200" href="/about"> About </a>
			<a class=" px-5 py-3 border dark:border-white border-black w-full md:w-48 text-center dark:text-white active:scale-95 duration-200" href="/contact"> Contact</a>
		</div>
	</section>
	<div class="h-fit flex flex-col w-full max-w-screen-2xl space-y-10">
		<p class="md:w-1/2 w-full text-lg font-light leading-relaxed text-center text-black">
			</p>
		<div class="flex h-full w-full flex-col justify-between p-5 md:p-10 gap-10">
			<h1 class="text-4xl">Featured Projects</h1>
			<div class="w-full flex flex-col md:flex-row gap-10 text-white">
				<a class="md:w-1/3 aspect-square overflow-hidden grid grid-cols-1 grid-rows-1 place-items-center justify-center parent object-cover" href="/projects/premier-tower">
					<div class="row-start-1 col-start-1 text-2xl z-10 h-full w-full bg-black bg-opacity-30 duration-150 md:opacity-0 child justify-start place-items-end p-5 transition-all">
						 <h1>Premier Tower<br/> <span class="text-sm">Building Development</span></h1>
					</div>
					<img class="col-start-1 row-start-1 h-full min-w-full" alt="test" src="https://www.premiertower.com.au/resources/images/home/main_tower_1.jpg" />
				</a>
				<a class="md:w-1/3 aspect-square overflow-hidden grid grid-cols-1 grid-rows-1 place-items-center justify-center parent" href="/projects/shangri-la">
					<div class="row-start-1 col-start-1 text-2xl z-10 h-full w-full bg-black bg-opacity-30 duration-150 md:opacity-0 child justify-start place-items-end p-5 transition-all">
						 <h1>Shangri La <br/> <span class="text-sm">Building Development</span></h1>
						</div>
					<img class="col-start-1 row-start-1 h-full" alt="test" src="https://images.unsplash.com/photo-1683790281028-120389677131?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2833&q=80" />
				</a>
				<a class="md:w-1/3 aspect-square overflow-hidden grid grid-cols-1 grid-rows-1 place-items-center justify-center parent" href="/projects/west-side-place">
					<div class="row-start-1 col-start-1 text-2xl z-10 h-full w-full bg-black bg-opacity-30 duration-150 md:opacity-0 child justify-start place-items-end p-5 transition-all">
						 <h1 class="px-5 py-2 bg-slate-900 leading-tight">West Side Place<br/> <span class="text-sm">Building Development</span></h1>
						</div>
					<img class="col-start-1 row-start-1 h-full" alt="test" src="https://westsideplace.com.au/wp-content/themes/wsp/dist/assets/images/apartments/WSP_view-01.jpg" />
				</a>
			</div>
			<a href="/projects">
				<h1 class="text-2xl uppercase underline-offset-[15px] hover:text-gray-400 duration-150 underline w-fit">View All Projects</h1>
			</a>
		</div>
		<div class="h-fit w-full flex flex-col p-5 md:p-10 gap-10 justify-evenly hidden">
			<h1 class="text-4xl">Our Approach</h1>
			<p class="md:w-1/2 w-full text-2xl font-light leading-relaxed">
				We understand the importance of minimising delays on building projects. 
			This is why we are dedicated to providing a fast and efficient floor preparation 
			service done by qualified and insured professionals with minimal interruptions.
				</p>
		</div>
	</div>
	<div class="md:h-[20rem] h-[10rem] w-full justify-center flex place-items-center bg-[url('https://images.unsplash.com/photo-1454117096348-e4abbeba002c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80')] bg-cover dark:hidden">
		<h1 class="text-4xl">Our Services</h1>
	</div>
	<div class="md:h-[20rem] h-[10rem] w-full justify-center place-items-center bg-[url('https://images.unsplash.com/photo-1496150458551-140441714f2f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80')] bg-center bg-cover hidden dark:flex">
		<h1 class="text-4xl">Our Services</h1>
	</div>
		<div class="h-fit w-full flex flex-col p-5 md:p-10 gap-10 justify-evenly ">
			<p class="md:w-1/2 w-full text-2xl font-light leading-relaxed">
				Panorama Flooring can act as a Subcontractor or work directly with Builders.
				Ready to provide all flooring services and materials necessary to complete any job, 
				no matter the size or complexity. We are experts in <span class="font-bold">Floor Griding & Leveling</span> with top of the line machinery to support our staff.
			</p>

			<!---
			<div class="w-full h-screen flex flex-row flex-wrap gap-5 justify-center">
				<div class="flex h-72 aspect-[3/2] justify-center place-items-center text-white  overflow-clip">
					<img class="h-full w-full hover:scale-[1.5] duration-[3000ms]" alt="test" src="/test.png">
				</div>
				<div class="flex h-56 aspect-[3/2] bg-slate-200 justify-center place-items-center bg-[url('/test.png')] bg-cover text-white">
					<h1>Appartment Blocks</h1>
				</div>
				<div class="flex h-56 aspect-[3/2] bg-slate-200 justify-center place-items-center bg-[url('/test.png')] bg-cover text-white">
					<h1>Hotels</h1>
				</div>
				<div class="flex h-56 aspect-[3/2] bg-slate-200 justify-center place-items-center bg-[url('/test.png')] bg-cover text-white">
					<h1>Office Buildings</h1>
				</div>
				<div class="flex h-56 aspect-[3/2] bg-slate-200 justify-center place-items-center bg-[url('/test.png')] bg-cover text-white">
					<h1>Warehouses</h1>
				</div>
				<div class="flex h-56 aspect-[3/2] bg-slate-200 justify-center place-items-center bg-[url('/test.png')] bg-cover text-white">
					<h1>Warehouses</h1>
				</div>
			</div>
			-->
		</div>
		<div class="flex h-fit flex-col md:flex-row p-5 md:p-10 justify-center gap-10">
			<div class="w-full h-full flex flex-col justify-evenly gap-20">
				<h1 class="text-4xl">Get In Touch</h1>
				<form class="flex flex-col w-full gap-5 dark:text-white text-black" method="POST" use:enhance>
					<div class="flex flex-row w-full gap-5">			
						<input class="w-full border  border-l-0 border-r-0 border-t-0 placeholder:text-gray-300 focus:ring-0 focus:outline-none bg-gray-700 bg-opacity-50 rounded-t-lg" type="text" placeholder="Your Name" required/>
						<input class="w-full  border  border-l-0 border-r-0 border-t-0  placeholder:text-gray-300 focus:ring-0 bg-gray-700 bg-opacity-50 rounded-t-lg" type="text" placeholder="Your Number" required/>
					</div>
					<input class="w-full  border border-l-0 border-r-0 border-t-0 placeholder:text-gray-300 focus:ring-0 bg-gray-700 bg-opacity-50 rounded-t-lg" type="text" placeholder="Your Email" required/>
					<textarea class="resize-none border-t-0 border-r-0 border-l-0 placeholder:text-gray-300 focus:ring-0 bg-gray-700 bg-opacity-50 rounded-t-lg"  rows="4" placeholder="Lorem ipsum dolor sit amet consectetur adipisicing elit." required/>
					<button class="rounded-lg px-5 py-3 border-gray-400 border w-full md:w-48 text-center active:scale-95 duration-200"> Send Message</button>

				</form>
			</div>
			<div class="h-full w-full flex justify-center place-items-center leading-loose text-lg font-light place-self-center">
				<p>
					We believe communication is key when it comes to delivering the right commercial flooring solution. It all starts here.
					If you have any questions about the flooring products or services we provide, please don't hesitate to contact us today.
				</p>
			</div>
		</div>
	
</div>


<style>

	.parent{
		display: grid;
	}

	.child{
		display: flex;
	}
	.parent:hover .child {
 		 opacity: 1
}
</style>
