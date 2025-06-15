<script>
	import { onMount } from 'svelte';

	let text = "MY NAME IS THANADON";
	let displayedText = '';
	let index = 0;
	let isDeleting = false;

	onMount(() => {
		typeWriter();
	});

	function typeWriter() {
		const typingSpeed = isDeleting ? 60 : 120;
		displayedText = text.slice(0, index);

		if (!isDeleting) {
			if (index < text.length) {
				index++;
			} else {
				isDeleting = true;
				setTimeout(typeWriter, 4000);
				return;
			}
		} else {
			if (index > 0) {
				index--;
			} else {
				isDeleting = false;
				setTimeout(typeWriter, 1000);
				return;
			}
		}

		setTimeout(typeWriter, typingSpeed);
	}
</script>

<div class="font-kanit min-h-screen bg-gradient-to-b from-white to-cyan-100/75 font-bold mt-49 flex justify-center text-center">
	<main class="w-96">
		<p class="text-2xl text-cyan-500 ">
			{displayedText}<span class="border-r-1 border-cyan-500 animate-pulse ml-1"></span>
		</p>
			<p class="w-full mt-7 ">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corrupti distinctio quam necessitatibus magni soluta nulla nisi eos totam, doloribus quaerat!</p>
			<div class="flex justify-center  mt-12">
				<div class="ring-container ">
					<div class="rotating-ring "></div>
					<img class="rounded-full border-4 border-white shadow-xl" width="200px" src="/favicon.png"  alt="">
				</div>
			</div>
			<div class="mt-56">
				<div class="text-7xl arrow-down "></div>
			</div>
	</main>
</div>
<div class="h-100"></div>
