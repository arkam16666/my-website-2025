<script>
	let ul = {
		Home: "HOME",
		Skill: "SKILL",
		Project: "PROJECT",
		About: "ABOUT",
		Game: "GAME"
	};

	let isOpen = false;
</script>


<div class="w-full flex justify-center px-4 fixed top-0 left-0 right-0 z-1">
	<nav
		class=" shadow-2xl mt-4 bg-transparent backdrop-blur-sm  rounded-3xl px-6 py-4 
               w-[75%] max-w-[90%] sm:max-w-[250px] md:max-w-[600px] lg:max-w-[700px] 
               transition-all duration-300 absolute">

		<div class="flex justify-between w-full items-center sm:hidden">
			<div class="text-xl font-bold text-gray-700">Menu</div>
			<button aria-label="toggle" on:click={() => (isOpen = !isOpen)} class="text-gray-600 focus:outline-none">
				<svg class="w-6 h-6" fill="none" stroke="currentColor"
					viewBox="0 0 24 24" xmlns="">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
						d="M4 6h16M4 12h16M4 18h16" />
				</svg>
			</button>
		</div>

		<ul class={`mt-4 sm:mt-0 font-mono text-center sm:text-xl lg:text-lg  text-black 
                    ${isOpen ? '' : 'hidden'} sm:flex sm:flex-row sm:justify-center sm:space-x-6 lg:space-x-18 `}>
			<li class="py-2 sm:py-0 ">
				<a href="#Home" class="relative underline-hover hover:text-cyan-500  transition-colors duration-300 block">{ul.Home}</a>
			</li>
			<li class="py-2 sm:py-0">
				<a href="#Skill" class="relative underline-hover hover:text-cyan-500 transition-colors duration-300 block">{ul.Skill}</a>
			</li>
			<li class="py-2 sm:py-0">
				<a href="#Project" class="relative underline-hover hover:text-cyan-500 transition-colors duration-300 block">{ul.Project}</a>
			</li>
			<li class="py-2 sm:py-0">
				<a href="#About" class="relative underline-hover hover:text-cyan-500 transition-colors duration-300 block">{ul.About}</a>
			</li>
			<li class="py-2 sm:py-0">
				<a href="#Game" class="relative underline-hover hover:text-cyan-500 transition-colors duration-300 block">{ul.Game}</a>
			</li>
		</ul>
	</nav>
</div>
