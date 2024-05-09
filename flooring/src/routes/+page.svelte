<script>

	import { enhance } from "$app/forms";
	import { Accordion, AccordionItem } from '@skeletonlabs/skeleton';
</script>

<div class="h-fit w-full justify-center flex flex-col place-items-center bg-white  dark:">
	<section id="hero" class="w-full md:h-screen h-[40rem] justify-center place-items-center flex bg-fixed bg-cover bg-bottom p-10 flex-col gap-10 bg-[url('https://images.unsplash.com/photo-1680754900504-bf6236cfc30f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=3133&q=80')] text-white">
		<div class="h-full w-full absolute bg-[#091426] bg-opacity-90">

		</div>
		<h1 class="text-6xl md:text-9xl text-center font-bold z-10">PANORAMA FLOORING</h1>
		<h1 class="text-3xl font-medium z-10">Quality above all else</h1>
		<p class="min-w-96 max-w-screen-md text-center text-lg hidden md:block z-10">We understand the importance of minimising delays on building projects. 
			This is why we are dedicated to providing a fast and efficient floor preparation 
			service done by qualified and insured professionals with minimal interruptions.
			</p>
		<div class="flex flex-col md:flex-row gap-5 md:gap-10 w-full justify-center cursor-pointer pointer-events-auto z-10">
			<a class=" px-5 py-3 border-white dark:bg-white bg-white text-[#091426] dark: w-full md:w-48 text-center active:scale-95 duration-200 rounded-lg" href="/about"> About </a>
			<a class=" px-5 py-3 border dark:border-white border-white w-full md:w-48 text-center  active:scale-95 duration-200 rounded-lg" href="/contact"> Contact</a>
		</div>
	</section>
	
	<div class="h-fit flex flex-col w-full max-w-screen-2xl bg-[#091426] text-white">
		<p class="md:w-1/2 w-full text-lg font-light leading-relaxed text-center ">
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
						 <h1 class="leading-tight">West Side Place<br/> <span class="text-sm">Building Development</span></h1>
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

	<div class="w-full h-fit overflow-x-scroll hide-scrollbar flex flex-col bg-white md:py-10 py-5">
		<div class="snap-x scroll-px-4 snap-mandatory scroll-smooth flex gap-4 overflow-x-auto px-4  hide-scrollbar">
			<div class="snap-center shrink-0 py-20 w-fit aspect-auto ">
				<img src="https://panoramaflooringimages.s3.ap-southeast-2.amazonaws.com/clogo1.jpg" class="aspect-auto h-14 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-fit aspect-auto ">
				<img src="https://panoramaflooringimages.s3.ap-southeast-2.amazonaws.com/clogo2.png" class="aspect-auto h-14 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-fit aspect-auto ">
				<img src="https://panoramaflooringimages.s3.ap-southeast-2.amazonaws.com/clogo3.png" class="aspect-auto h-14 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-fit aspect-auto ">
				<img src="https://panoramaflooringimages.s3.ap-southeast-2.amazonaws.com/clogo4.png" class="aspect-auto h-14 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-fit aspect-auto ">
				<img src="https://panoramaflooringimages.s3.ap-southeast-2.amazonaws.com/clogo5.jpg" class="aspect-auto h-14 rounded-xl">
			</div>
			<div class="snap-center shrink-0 py-20 w-fit aspect-auto ">
				<img src="https://panoramaflooringimages.s3.ap-southeast-2.amazonaws.com/clogo6.png" class="aspect-auto h-14 rounded-xl w-full">
			</div>
			<div class="snap-center shrink-0 py-20 w-fit aspect-auto ">
				<img src="https://panoramaflooringimages.s3.ap-southeast-2.amazonaws.com/clogo7.jpg" class="aspect-auto h-14 rounded-xl">
			</div>
		</div>
	</div>
	<div class=" flex flex-col justify-center w-full h-fit gap-5 p-5 ">
		<div class="flex flex-col md:flex-row justify-center gap-5 ">
			<div class="w-full h-96 bg-pink rounded-xl grid grid-cols-1 grid-rows-1 overflow-hidden">
				<div class="w-full h-full bg-slate-900 bg-opacity-50 col-start-1 row-start-1 z-10">

				</div>
				<img src="SelfLevel.jpg" class="h-full col-start-1 row-start-1">
				<div class="row-start-1 col-start-1 place-self-end text-white z-20 w-full p-5 gap-2 flex-col flex text-center">
					<h2 class="h1">Floor Levelling</h2>
					<p class="hidden">Our experts will help you choose the right levelling compound for your job.
						We can level any area no matter the size or complexity, specializing in levelling apartments,
						common areas, hotels and more.
					</p>				
				</div>



			</div>
			<div class="w-full h-96 bg-pink rounded-xl grid grid-cols-1 grid-rows-1 overflow-hidden">
				<div class="w-full h-full bg-slate-900 bg-opacity-50 col-start-1 row-start-1 z-10">

				</div>
				<img src="Griding.jpg" class="h-full w-auto col-start-1 row-start-1">
				<div class="row-start-1 col-start-1 place-self-end text-white z-20 w-full p-5 gap-2 flex-col flex text-center">
					<h2 class="h1">Concrete Grinding and Sealing</h2>
					<p class="hidden">Our experts will help you choose the right levelling compound for your job.
						We can level any area no matter the size or complexity, specializing in levelling apartments,
						common areas, hotels and more.
					</p>			
				</div>

			</div>
			

		</div>
		<div class="w-full h-fit bg-rounded-lg p-5">
			<p class="w-full text-2xl font-light leading-relaxed">
				Panorama Flooring can act as a Subcontractor or work directly with Builders.
				Ready to provide all flooring services and materials necessary to complete any job, 
				no matter the size or complexity. We are experts in <span class="font-bold">Floor Grinding & Levelling</span> with top of the line machinery to support our staff.
			</p>
		</div>

	</div>
	
	<div class="flex md:grid md:grid-cols-3 md:grid-rows-2 flex-col justify-center w-full h-fit gap-10 p-5 md:p-10 bg-white">
		<div class="flex md:col-start-1 md:col-span-2 md:row-span-1 w-full md:flex-row flex-col justify-evenly place-items-center bg-gray-100 rounded-xl p-5 gap-5 hidden">
			<div class="aspect-square w-full md:w-2/3 bg-white rounded-lg flex justify-center place-items-center overflow-hidden">
				<img src="SelfLevel.jpg" class="h-full">
			</div>
			<div class="flex flex-col gap-5 justify-evenly h-full">
				<h2 class="h1">Floor Levelling</h2>
				<p>Our experts will help you choose the right levelling compound for your job.
					We can level any area no matter the size or complexity, specializing in levelling apartments,
					common areas, hotels and more.
				</p>
			</div>
		</div>
		<div class="flex md:col-start-1 md:col-span-2 md:row-span-1 w-full md:flex-row flex-col justify-evenly place-items-center bg-gray-100 rounded-xl p-5 gap-5 hidden">
			<div class="aspect-square w-full md:w-2/3 bg-white rounded-lg flex justify-center place-items-center overflow-hidden">
				<img src="Griding.jpg" class="h-full">
			</div>
			<div class="flex flex-col h-full justify-evenly gap-5">
				<h2 class="h1">Concrete Grinding and Sealing</h2>
				<p>Our experts will help you choose the right levelling compound for your job.
					We can level any area no matter the size or complexity, specializing in levelling apartments,
					common areas, hotels and more.
				</p>
			</div>
		</div>
		<div class="flex w-full md:col-start-3 md:col-span-1 md:row-span-2 md:row-start-1 bg-gray-100 rounded-xl p-5 hidden">
			<p class="w-full text-2xl font-light leading-relaxed">
				Panorama Flooring can act as a Subcontractor or work directly with Builders.
				Ready to provide all flooring services and materials necessary to complete any job, 
				no matter the size or complexity. We are experts in <span class="font-bold">Floor Griding & Levelling</span> with top of the line machinery to support our staff.
			</p>
		</div>
	</div>
	<div class="h-fit flex flex-col w-full max-w-screen-2xl">
		<p class="md:w-1/2 w-full text-lg font-light leading-relaxed text-center "></p>
		<div class="flex h-full w-full flex-col justify-between p-5 md:p-10 gap-10">
			<div class="w-full flex  justify-center">
				<div class="md:flex grid grid-cols-2 grid-flow-row md:flex-row gap-10 bg-gray-100 p-5 justify-center rounded-xl">
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 48 48"><g fill="none" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"><circle cx="24" cy="11" r="7" fill="#2F88FF"/><path d="M4 41C4 32.1634 12.0589 25 22 25"/><path fill="#2F88FF" d="M28 29.2C28 28.1333 35 26 35 26C35 26 42 28.1333 42 29.2C42 37.7333 35 42 35 42C35 42 28 37.7333 28 29.2Z"/></g></svg>						<h1 class="text-xl">Owner Operated</h1>
					</div>
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 48 48"><g fill="none" stroke-linejoin="round" stroke-width="4"><path fill="#2F88FF" stroke="#000" d="M24 44C35.0457 44 44 35.0457 44 24C44 12.9543 35.0457 4 24 4C12.9543 4 4 12.9543 4 24C4 35.0457 12.9543 44 24 44Z"/><path stroke="#fff" stroke-linecap="round" d="M24 35C29 35 31 31 31 31H17C17 31 19 35 24 35Z"/><path stroke="#fff" stroke-linecap="round" d="M31 18V22"/><path stroke="#fff" stroke-linecap="round" d="M17 18V22"/></g></svg>						<h1 class="text-xl">Full Service</h1>
					</div>
					
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 48 48"><g fill="none"><path fill="#2F88FF" d="M36 32C36 28.446 34.455 25.2529 32 23.0556C29.877 21.1554 27.0734 20 24 20C20.9266 20 18.123 21.1554 16 23.0556C13.545 25.2529 12 28.446 12 32C12 38.6274 17.3726 44 24 44C30.6274 44 36 38.6274 36 32Z"/><path fill="#2F88FF" d="M16 4H32V20V23.0556C29.877 21.1554 27.0734 20 24 20C20.9266 20 18.123 21.1554 16 23.0556V20V4Z"/><path stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="4" d="M16 4H32M16 4H8V14L16 20M16 4V20M32 4H40V14L32 20M32 4V20M16 23.0556C18.123 21.1554 20.9266 20 24 20C27.0734 20 29.877 21.1554 32 23.0556M16 23.0556C13.545 25.2529 12 28.446 12 32C12 38.6274 17.3726 44 24 44C30.6274 44 36 38.6274 36 32C36 28.446 34.455 25.2529 32 23.0556M16 23.0556V20M32 23.0556V20"/><path stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="4" d="M32 4H40V14L32 20"/><path stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="4" d="M16 4H8V14L16 20"/><path fill="#2F88FF" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="4" d="M36 32C36 28.446 34.455 25.2529 32 23.0556C29.877 21.1554 27.0734 20 24 20C20.9266 20 18.123 21.1554 16 23.0556C13.545 25.2529 12 28.446 12 32C12 38.6274 17.3726 44 24 44C30.6274 44 36 38.6274 36 32Z"/><path fill="#2F88FF" stroke="#000" stroke-linecap="round" stroke-linejoin="round" stroke-width="4" d="M16 4.00009H32V20.0001V23.0557C29.877 21.1555 27.0734 20.0001 24 20.0001C20.9266 20.0001 18.123 21.1555 16 23.0557V20.0001V4.00009Z"/><path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="4" d="M24 37V27L22 28M24 37H26M24 37H22"/></g></svg>
						<h1 class="text-xl">Premimum Materials</h1>
					</div>
					
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 48 48"><g fill="none" stroke="#000" stroke-linejoin="round" stroke-width="4"><path stroke-linecap="round" d="M41.7796 20.6066C42.0324 18.9108 41.9495 17.1747 41.5309 15.5054C40.978 13.3002 39.8392 11.2118 38.1147 9.4873C36.3902 7.76281 34.3018 6.62409 32.0967 6.07115C30.4274 5.65257 28.6912 5.56967 26.9954 5.82245"/><path stroke-linecap="round" d="M34.1897 19.8035C34.4605 17.9869 33.8967 16.0699 32.4983 14.6715C31.0998 13.2731 29.1829 12.7092 27.3663 12.98"/><path fill="#2F88FF" d="M14.3757 8.79424C15.1022 8.79424 15.7716 9.1883 16.1243 9.8235L18.5707 14.2303C18.891 14.8073 18.9061 15.5052 18.6109 16.0955L16.2541 20.8091C16.2541 20.8091 16.9371 24.3206 19.7955 27.179C22.654 30.0374 26.1536 30.7086 26.1536 30.7086L30.8665 28.3522C31.4572 28.0568 32.1556 28.0721 32.7328 28.393L37.1521 30.85C37.7868 31.2028 38.1803 31.8719 38.1803 32.598V37.6715C38.1803 40.2552 35.7804 42.1213 33.3323 41.2952C28.3044 39.5987 20.4997 36.3685 15.5529 31.4216C10.606 26.4748 7.37579 18.6701 5.67928 13.6422C4.85325 11.1941 6.71934 8.79424 9.30299 8.79424H14.3757Z"/></g></svg>
						<h1 class="text-xl">Competitive Pricing</h1>
					</div>
					
					<div class="flex gap-5 justify-center aspect-square rounded-lg flex-col place-items-center p-3 text-center">
<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 48 48"><g fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="4"><path fill="#2F88FF" stroke="#000" d="M10 44H38C39.1046 44 40 43.1046 40 42V14H30V4H10C8.89543 4 8 4.89543 8 6V42C8 43.1046 8.89543 44 10 44Z"/><path stroke="#000" d="M30 4L40 14"/><path fill="#43CCF8" stroke="#fff" d="M24 19L26.5234 24.5269L32.5595 25.2188L28.0829 29.3266L29.2901 35.2812L24 32.293L18.7099 35.2812L19.9171 29.3266L15.4405 25.2188L21.4766 24.5269L24 19Z"/></g></svg>
						<h1 class="text-xl">Free Quotes</h1>
					</div>
				</div>
				
				
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
