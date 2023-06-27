<script>

	import { enhance } from "$app/forms";

</script>

<div class="h-fit w-full justify-center flex flex-col place-items-center bg-slate-100 text-gray-500 gap-10 ">
	<section id="hero" class="w-full h-screen justify-center place-items-center flex bg-[url('/test.png')] bg-cover bg-center">
	</section>
	<div class="h-fit flex flex-col w-full max-w-screen-2xl gap-10">
		<div class="h-96 w-full flex place-items-center p-5 md:p-10">
			<p class="md:w-1/2 w-full text-2xl font-light leading-relaxed text-gray-500">
			We understand the importance of minimising delays on building projects. 
			This is why we are dedicated to providing a fast and efficient floor preparation 
			service done by qualified and insured professionals with minimal interruptions.
			</p>
		</div>
		<div class="flex h-screen w-full flex-col justify-between p-5 md:p-10">
			<h1 class="text-4xl">Featured Projects</h1>
			<div class="h-2/3 w-full bg-slate-200 p-5 flex justify-center">
				<div class="grid grid-cols-3 w-fit gap-10 overflow-hidden">
					<div class="bg-pink-200 h-full w-96 shrink-0"></div>
					<div class="bg-green-200 h-full w-96"></div>
					<div class="bg-yellow-200 h-full w-96"></div>
				</div>

			</div>
			<h2 class="text-2xl uppercase underline-offset-[15px] hover:text-gray-400 duration-150 underline"><a href="/projects">View All Projects</a></h2>
		</div>
		<div class="min-h-screen max-h-fit w-full flex flex-col p-5 md:p-10 gap-10 justify-evenly">
			<h1 class="text-4xl">Services</h1>
			<p class="md:w-1/2 w-full text-2xl font-light leading-relaxed text-gray-500">
				Panorama Flooring can act as a Subcontractor or work directly with Builders.
				Ready to provide all flooring services and materials necessary to complete any job, 
				no matter the size or complexity. We are experts in <span class="font-bold">Floor Griding & Leveling</span> with top of the line machinery to support our staff.
			</p>
			<div class="w-full h-full flex flex-row flex-wrap gap-5 justify-center">
				<!--
				<div class="flex h-56 aspect-[3/2] justify-center place-items-center text-white  overflow-clip">
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
				-->
			</div>
		</div>
		<div class="md:h-[calc(100vh-5rem)] h-fit flex flex-col md:flex-row gap-20 p-5 md:p-10">
			<div class="w-full h-full flex flex-col justify-evenly gap-20">
				<h1 class="text-4xl">Get In Touch</h1>
				<form class="flex flex-col w-full gap-5 " method="POST" use:enhance>
					<div class="flex flex-row w-full gap-5">			
						<input class="w-full bg-transparent border border-b-black border-l-0 border-r-0 border-t-0 text-black placeholder:text-gray-500 focus:ring-0 focus:outline-none" type="text" placeholder="Your Name" required/>
						<input class="w-full bg-transparent border border-b-black border-l-0 border-r-0 border-t-0 text-black placeholder:text-gray-500 focus:ring-0 " type="text" placeholder="Your Number" required/>
					</div>
					<input class="w-full bg-transparent border border-b-black border-l-0 border-r-0 border-t-0 text-black placeholder:text-gray-500 focus:ring-0 " type="text" placeholder="Your Email" required/>
					<textarea class="resize-none border-t-0 border-r-0 border-l-0 placeholder:text-gray-500 focus:ring-0 bg-transparent "  rows="4" placeholder="Lorem ipsum dolor sit amet consectetur adipisicing elit." required/>
					<button class="text-base px-10 btn btn-sm  rounded-none place-self-start bg-slate-300 ">Send Message</button>
				</form>

			</div>
			<div class="h-full w-full flex justify-center place-items-center leading-loose text-lg font-light">
				<p>
					We believe communication is key when it comes to delivering the right commercial flooring solution. It all starts here.
					If you have any questions about the flooring products or services we provide, please don't hesitate to contact us today.
				</p>
			</div>
		</div>
	</div>
</div>
