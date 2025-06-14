<script>
	let ul = {
		Home: "Home",
		Skill: "Skill",
		Project: "Project",
		About: "About",
		Game: "Game"
	};

	let isOpen = false;
</script>


<div class="w-full flex justify-center  px-4">
	<nav
		class=" shadow-2xl mt-4 bg-transparent backdrop-blur-sm  rounded-3xl px-6 py-4 
               w-[75%] max-w-[90%] sm:max-w-[250px] md:max-w-[600px] lg:max-w-[700px] 
               transition-all duration-300 absolute">

		<!-- Mobile toggle button -->
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

		<!-- Nav items -->
		<ul class={`mt-4 sm:mt-0 font-bold text-center sm:text-xl lg:text-2xl  text-black 
                    ${isOpen ? '' : 'hidden'} sm:flex sm:flex-row sm:justify-center sm:space-x-6 lg:space-x-20`}>
			<li class="py-2 sm:py-0">
				<a href="#Home" class="hover:text-blue-600 transition-colors duration-200 block">{ul.Home}</a>
			</li>
			<li class="py-2 sm:py-0">
				<a href="#Skill" class="hover:text-blue-600 transition-colors duration-200 block">{ul.Skill}</a>
			</li>
			<li class="py-2 sm:py-0">
				<a href="#Project" class="hover:text-blue-600 transition-colors duration-200 block">{ul.Project}</a>
			</li>
			<li class="py-2 sm:py-0">
				<a href="#About" class="hover:text-blue-600 transition-colors duration-200 block">{ul.About}</a>
			</li>
			<li class="py-2 sm:py-0">
				<a href="#Game" class="hover:text-blue-600 transition-colors duration-200 block">{ul.Game}</a>
			</li>
		</ul>
	</nav>
</div>
