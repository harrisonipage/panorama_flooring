<script>

	import { enhance } from "$app/forms";

</script>
<div class="h-full w-full flex flex-col bg-black text-white">
    <div class="flex min-h-screen flex-col md:flex-row p-5 md:p-10 justify-center place-items-center gap-10">
        <div class="w-full h-full flex flex-col justify-evenly gap-20">
            <h1 class="text-4xl">Get In Touch</h1>
            <form class="flex flex-col w-full gap-5 text-white" method="POST" use:enhance>
                <div class="flex flex-row w-full gap-5">			
                    <input class="w-full bg-transparent border  border-l-0 border-r-0 border-t-0 placeholder:text-gray-300 focus:ring-0 focus:outline-none bg-gray-700 bg-opacity-50 rounded-t-lg" type="text" placeholder="Your Name" required/>
                    <input class="w-full bg-transparent border  border-l-0 border-r-0 border-t-0  placeholder:text-gray-300 focus:ring-0 bg-gray-700 bg-opacity-50 rounded-t-lg" type="text" placeholder="Your Number" required/>
                </div>
                <input class="w-full bg-transparent border border-l-0 border-r-0 border-t-0  placeholder:text-gray-300 focus:ring-0 bg-gray-700 bg-opacity-50 rounded-t-lg" type="text" placeholder="Your Email" required/>
                <textarea class="resize-none border-t-0 border-r-0 border-l-0 placeholder:text-gray-300 focus:ring-0 bg-gray-700 bg-opacity-50 rounded-t-lg"  rows="4" placeholder="Lorem ipsum dolor sit amet consectetur adipisicing elit." required/>
                <button class="text-base px-10 btn btn-sm  rounded-none place-self-start bg-slate-700 ">Send Message</button>
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