<script lang="ts">
	import { goto } from '$app/navigation';

	function openMenu() {
		goto('/menu');
	}
</script>

<svelte:head>
	<title>Save the Date | Markis + Olivia</title>
</svelte:head>

<main class="min-h-screen bg-white">
	<!-- Header with hamburger menu and logo - STICKY -->
	<header class="fixed top-0 left-0 right-0 z-50 bg-white p-6 flex items-start justify-between">
		<button onclick={openMenu} class="p-2 hover:bg-gray-100 rounded transition-colors">
			<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
			</svg>
		</button>
		<div class="font-script text-2xl text-black text-center leading-tight">
			M<br />+<br />O
		</div>
		<div class="w-10"></div><!-- Spacer for centering -->
	</header>

	<!-- Content - with padding for fixed header -->
	<div class="max-w-md mx-auto px-6 sm:px-8 py-8 text-center pt-32">
		<!-- The Date -->
		<section class="mb-10">
			<h2 class="font-script text-[28pt] sm:text-[40pt] text-black mb-1">The Date:</h2>
			<p class="font-sans text-[14pt] sm:text-[20pt] text-black">Thursday, October 22nd 2026</p>
		</section>

		<!-- Where -->
		<section class="mb-10">
			<h2 class="font-script text-[28pt] sm:text-[40pt] text-black mb-1">Where:</h2>
			<p class="font-sans text-[14pt] sm:text-[20pt] text-black">Mexico City, CDMX</p>
		</section>

		<!-- The Schedule -->
		<section class="mb-12">
			<h2 class="font-script text-[28pt] sm:text-[40pt] text-black mb-2">The Schedule:</h2>
			<div class="space-y-1 font-sans text-[14pt] sm:text-[20pt] text-black">
				<p>Wednesday - Welcome Gathering</p>
				<p>Thursday - Wedding</p>
				<p>Friday+Saturday - Hangout</p>
				<p>with the newlyweds</p>
			</div>
		</section>

		<!-- Buttons -->
		<div class="space-y-6 flex flex-col items-center">
			<a
				href="/more-info"
				class="group inline-flex items-center justify-between w-48 sm:w-56 px-4 py-2 border border-black bg-white hover:bg-gray-50 transition-colors duration-300 shadow-[5px_5px_0px_0px_#B6531B,5px_5px_0px_1px_black]"
			>
				<span class="font-script text-black text-[16pt] sm:text-[20pt]">More info</span>
				<svg class="w-5 h-5 text-black group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
				</svg>
			</a>

			<a
				href="/rsvp"
				class="group inline-flex items-center justify-between w-48 sm:w-56 px-4 py-2 border border-black bg-white hover:bg-gray-50 transition-colors duration-300 shadow-[5px_5px_0px_0px_#B6531B,5px_5px_0px_1px_black]"
			>
				<span class="font-script text-black text-[16pt] sm:text-[20pt]">Pre RSVP</span>
				<svg class="w-5 h-5 text-black group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
				</svg>
			</a>
		</div>
	</div>
</main>
