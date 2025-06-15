<script>
	import { onMount } from 'svelte';
	import { fly } from 'svelte/transition';
	let text = 'MY NAME IS THANADON';
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

<div
	class="font-kanit mt-49 flex h-[78.5vh] justify-center bg-gradient-to-b from-white to-cyan-100/75 text-center font-bold"
>
	<main class="w-96">
		<p class="text-2xl text-cyan-500">
			{displayedText}<span class="ml-1 animate-pulse border-r-1 border-cyan-500"></span>
		</p>
		<p class="mt-7 w-full">
			Lorem, ipsum dolor sit amet consectetur adipisicing elit. Corrupti distinctio quam
			necessitatibus magni soluta nulla nisi eos totam, doloribus quaerat!
		</p>
		<div class="mt-12 flex justify-center">
			<div class="ring-container" data-aos="zoom-out">
				<div class="rotating-ring" ></div>
				<img
					src="/favicon.png"
					alt="Logo"
					width="200"
					data-aos="zoom-out"
					class="rounded-full border-4 border-white shadow-xl transition duration-300 ease-in-out"
				/>
			</div>
		</div>
	</main>
</div>
