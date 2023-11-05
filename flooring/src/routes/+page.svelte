<script>

	import { enhance } from "$app/forms";
	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';
</script>

<div class="h-fit w-full justify-center flex flex-col place-items-center bg-white text-black dark:text-black">
	<section id="hero" class="w-full h-screen justify-center place-items-center flex bg-fixed bg-cover bg-bottom text-black p-10 flex-col gap-10 bgz-[url('https://images.unsplash.com/photo-1680754900504-bf6236cfc30f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=3133&q=80')] bg-gray-100">
		<h1 class="text-6xl md:text-9xl text-center font-bold">PANORAMA FLOORING</h1>
		<h1 class="text-3xl font-medium">Quality above all else</h1>
		<p class="min-w-96 max-w-screen-md text-center text-lg hidden md:block">We understand the importance of minimising delays on building projects. 
			This is why we are dedicated to providing a fast and efficient floor preparation 
			service done by qualified and insured professionals with minimal interruptions.
			</p>
		<div class="flex flex-col md:flex-row gap-5 md:gap-10 w-full justify-center cursor-pointer pointer-events-auto">
			<a class=" px-5 py-3 border-gray-400 dark:bg-white bg-black text-white dark:text-black w-full md:w-48 text-center active:scale-95 duration-200 rounded-lg" href="/about"> About </a>
			<a class=" px-5 py-3 border dark:border-white border-black w-full md:w-48 text-center text-black active:scale-95 duration-200 rounded-lg" href="/contact"> Contact</a>
		</div>
	</section>
	
	<div class="h-fit flex flex-col w-full max-w-screen-2xl bg-gray-100">
		<p class="md:w-1/2 w-full text-lg font-light leading-relaxed text-center text-black">
			</p>
		<div class="flex h-full w-full flex-col justify-between p-5 md:p-10 gap-10">
			<h1 class="text-4xl">Featured Projects</h1>
			<div class="w-full flex flex-col md:flex-row gap-10 text-white">
				<a class="md:w-1/3 aspect-square overflow-hidden grid grid-cols-1 grid-rows-1 place-items-center justify-center parent object-cover rounded-xl" href="/projects/premier-tower">
					<div class="row-start-1 col-start-1 text-2xl z-10 h-full w-full bg-black bg-opacity-30 duration-150 md:opacity-0 child justify-start place-items-end p-5 transition-all">
						 <h1>Premier Tower<br/> <span class="text-sm">Building Development</span></h1>
					</div>
					<img class="col-start-1 row-start-1 h-full min-w-full" alt="test" src="https://www.premiertower.com.au/resources/images/home/main_tower_1.jpg" />
				</a>
				<a class="md:w-1/3 aspect-square overflow-hidden grid grid-cols-1 grid-rows-1 place-items-center justify-center parent rounded-xl" href="/projects/shangri-la">
					<div class="row-start-1 col-start-1 text-2xl z-10 h-full w-full bg-black bg-opacity-30 duration-150 md:opacity-0 child justify-start place-items-end p-5 transition-all">
						 <h1>Shangri La <br/> <span class="text-sm">Building Development</span></h1>
						</div>
					<img class="col-start-1 row-start-1 h-full" alt="test" src="https://images.unsplash.com/photo-1683790281028-120389677131?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2833&q=80" />
				</a>
				<a class="md:w-1/3 aspect-square overflow-hidden grid grid-cols-1 grid-rows-1 place-items-center justify-center parent rounded-xl" href="/projects/west-side-place">
					<div class="row-start-1 col-start-1 text-2xl z-10 h-full w-full bg-black bg-opacity-30 duration-150 md:opacity-0 child justify-start place-items-end p-5 transition-all">
						 <h1 class="px-5 py-2 bg-slate-900 leading-tight">West Side Place<br/> <span class="text-sm">Building Development</span></h1>
						</div>
					<img class="col-start-1 row-start-1 h-full" alt="test" src="https://images.unsplash.com/photo-1626277828338-48bcc0272f1f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2936&q=80" />
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
	<div class="h-fit flex flex-col w-full max-w-screen-2xl space-y-10">
		<p class="md:w-1/2 w-full text-lg font-light leading-relaxed text-center text-black"></p>
		<div class="flex h-full w-full flex-col justify-between p-5 md:p-10 gap-10">
			<div class="w-full flex text-black justify-center">
				<div class="flex flex-col md:flex-row gap-10 bg-gray-100 p-5 justify-center rounded-xl">
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
						<svg class="w-full aspect-square" xmlns="http://www.w3.org/2000/svg" width="150" height="150" viewBox="0 0 24 24"><path fill="currentColor" d="M9.775 12q-.9 0-1.5-.675T7.8 9.75l.325-2.45q.2-1.425 1.3-2.363T12 4q1.475 0 2.575.938t1.3 2.362l.325 2.45q.125.9-.475 1.575t-1.5.675h-4.45Zm0-2h4.45L13.9 7.6q-.1-.7-.637-1.15T12 6q-.725 0-1.263.45T10.1 7.6L9.775 10ZM12 10Zm-8 8v-.8q0-.85.438-1.563T5.6 14.55q1.55-.775 3.15-1.163T12 13q1.65 0 3.25.388t3.15 1.162q.725.375 1.163 1.088T20 17.2v.8q0 .825-.588 1.413T18 20H6q-.825 0-1.413-.588T4 18Zm2 0h12v-.8q0-.275-.138-.5t-.362-.35q-1.35-.675-2.725-1.012T12 15q-1.4 0-2.775.338T6.5 16.35q-.225.125-.363.35T6 17.2v.8Zm6 0Z"/></svg>
						<h1 class="text-xl">Owner Operated</h1>
					</div>
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
						<svg class="w-full aspect-square" xmlns="http://www.w3.org/2000/svg" width="150" height="150" viewBox="0 0 24 24"><path fill="currentColor" d="M9.775 12q-.9 0-1.5-.675T7.8 9.75l.325-2.45q.2-1.425 1.3-2.363T12 4q1.475 0 2.575.938t1.3 2.362l.325 2.45q.125.9-.475 1.575t-1.5.675h-4.45Zm0-2h4.45L13.9 7.6q-.1-.7-.637-1.15T12 6q-.725 0-1.263.45T10.1 7.6L9.775 10ZM12 10Zm-8 8v-.8q0-.85.438-1.563T5.6 14.55q1.55-.775 3.15-1.163T12 13q1.65 0 3.25.388t3.15 1.162q.725.375 1.163 1.088T20 17.2v.8q0 .825-.588 1.413T18 20H6q-.825 0-1.413-.588T4 18Zm2 0h12v-.8q0-.275-.138-.5t-.362-.35q-1.35-.675-2.725-1.012T12 15q-1.4 0-2.775.338T6.5 16.35q-.225.125-.363.35T6 17.2v.8Zm6 0Z"/></svg>
						<h1 class="text-xl">Full Service</h1>
					</div>
					
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
						<svg class="w-full aspect-square" xmlns="http://www.w3.org/2000/svg" width="150" height="150" viewBox="0 0 24 24"><path fill="currentColor" d="m9.2 15.6l2.8-2.1l2.75 2.1l-1.05-3.4l2.8-2.2h-3.4L12 6.6L10.9 10H7.5l2.75 2.2l-1.05 3.4ZM12 22q-3.475-.875-5.737-3.988T4 11.1V5l8-3l8 3v6.1q0 3.8-2.263 6.913T12 22Zm0-2.1q2.6-.825 4.3-3.3t1.7-5.5V6.375l-6-2.25l-6 2.25V11.1q0 3.025 1.7 5.5t4.3 3.3Zm0-7.9Z"/></svg>
						<h1 class="text-xl">Premimum Materials</h1>
					</div>
					
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
						<svg class="w-full aspect-square" xmlns="http://www.w3.org/2000/svg" width="150" height="150" viewBox="0 0 24 24"><path fill="currentColor" d="m9.2 15.6l2.8-2.1l2.75 2.1l-1.05-3.4l2.8-2.2h-3.4L12 6.6L10.9 10H7.5l2.75 2.2l-1.05 3.4ZM12 22q-3.475-.875-5.737-3.988T4 11.1V5l8-3l8 3v6.1q0 3.8-2.263 6.913T12 22Zm0-2.1q2.6-.825 4.3-3.3t1.7-5.5V6.375l-6-2.25l-6 2.25V11.1q0 3.025 1.7 5.5t4.3 3.3Zm0-7.9Z"/></svg>
						<h1 class="text-xl">Competitive Pricing</h1>
					</div>
					
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
						<svg class="w-full aspect-square" xmlns="http://www.w3.org/2000/svg" width="150" height="150" viewBox="0 0 24 24"><path fill="currentColor" d="M12 4q3.35 0 5.675 2.325T20 12q0 3.35-2.325 5.675T12 20q-3.35 0-5.675-2.325T4 12q0-3.35 2.325-5.675T12 4Zm0 14q2.5 0 4.25-1.75T18 12q0-2.5-1.75-4.25T12 6Q9.5 6 7.75 7.75T6 12q0 2.5 1.75 4.25T12 18Zm0-2.5q1.2 0 2.15-.688T15.5 13h-7q.4 1.125 1.35 1.813T12 15.5ZM8.5 10q0 .425.288.713T9.5 11q.425 0 .713-.288T10.5 10q0-.425-.288-.713T9.5 9q-.425 0-.713.288T8.5 10Zm5 0q0 .425.288.713T14.5 11q.425 0 .713-.288T15.5 10q0-.425-.288-.713T14.5 9q-.425 0-.713.288T13.5 10ZM1 6V4q0-1.25.875-2.125T4 1h2v2H4q-.425 0-.713.288T3 4v2H1Zm3 17q-1.25 0-2.125-.875T1 20v-2h2v2q0 .425.288.713T4 21h2v2H4Zm14 0v-2h2q.425 0 .713-.288T21 20v-2h2v2q0 1.25-.875 2.125T20 23h-2Zm3-17V4q0-.425-.288-.713T20 3h-2V1h2q1.25 0 2.125.875T23 4v2h-2Zm-9 6Z"/></svg>
						<h1 class="text-xl">Free Quotes</h1>
					</div>
				</div>
				
				
			</div>
		</div>
	</div>
	
	<div class="flex md:grid md:grid-cols-3 md:grid-rows-2 flex-col justify-center w-full h-fit gap-10 p-5 md:p-10 bg-white">
		<div class="flex md:col-start-1 md:col-span-2 md:row-span-1 w-full md:flex-row flex-col justify-evenly place-items-center bg-gray-100 rounded-xl p-5 gap-5">
			<div class="aspect-square w-full md:w-2/3 bg-white rounded-lg flex justify-center place-items-center overflow-hidden">
				<img src="SelfLevel.jpg" class="h-full">
			</div>
			<div class="flex flex-col gap-5 justify-evenly h-full">
				<h2 class="h1">Floor Leveling</h2>
				<p>Our experts will help you choose the right levelling compound for your job.
					We can level any area no matter the size or complexity, specializing in levelling apartments,
					common areas, hotels and more.
				</p>
			</div>
		</div>
		<div class="flex md:col-start-1 md:col-span-2 md:row-span-1 w-full md:flex-row flex-col justify-evenly place-items-center bg-gray-100 rounded-xl p-5 gap-5">
			<div class="aspect-square w-full md:w-2/3 bg-white rounded-lg flex justify-center place-items-center overflow-hidden">
				<img src="Griding.jpg" class="h-full">
			</div>
			<div class="flex flex-col h-full justify-evenly gap-5">
				<h2 class="h1">Concrete Grind and Sealing</h2>
				<p>Our experts will help you choose the right levelling compound for your job.
					We can level any area no matter the size or complexity, specializing in levelling apartments,
					common areas, hotels and more.
				</p>
			</div>
		</div>
		<div class="flex w-full md:col-start-3 md:col-span-1 md:row-span-2 md:row-start-1 bg-gray-100 rounded-xl p-5">
			<p class="w-full text-2xl font-light leading-relaxed">
				Panorama Flooring can act as a Subcontractor or work directly with Builders.
				Ready to provide all flooring services and materials necessary to complete any job, 
				no matter the size or complexity. We are experts in <span class="font-bold">Floor Griding & Leveling</span> with top of the line machinery to support our staff.
			</p>
		</div>
	</div>
	<div class="w-full h-fit overflow-x-scroll hide-scrollbar flex flex-col bg-white md:py-10 py-5">
		<div class="w-full h-full px-5 md:px-10">
			<h1 class="text-4xl">Our Clients</h1>
		</div>
		<div class="snap-x scroll-px-4 snap-mandatory scroll-smooth flex gap-4 overflow-x-auto px-4  hide-scrollbar">
			<div class="snap-center shrink-0 py-20 w-full md:w-96 aspect-auto ">
				<img src="coles.png" class="aspect-auto h-40 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-full md:w-96 aspect-auto ">
				<img src="harris.png" class="aspect-auto h-40 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-full md:w-96 aspect-auto ">
				<img src="hickory.png" class="aspect-auto h-40 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-full md:w-96 aspect-auto ">
				<img src="lendlease.png" class="aspect-auto h-40 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-full md:w-96 aspect-auto ">
				<img src="mirvac.png" class="aspect-auto h-40 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-full md:w-96 aspect-auto ">
				<img src="probuild.png" class="aspect-auto h-40 rounded-xl w-full">
			</div>
			<div class="snap-center shrink-0 py-20 w-full md:w-96 aspect-auto ">
				<img src="mulitplex.png" class="aspect-auto h-40 rounded-xl">
			</div>
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
