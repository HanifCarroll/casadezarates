<script lang="ts">
	import Header from '$lib/components/Header.svelte';
</script>

<svelte:head>
	<title>Save the Date | Markis + Olivia</title>
</svelte:head>

<div class="min-h-screen bg-white flex flex-col">
	<Header bgClass="bg-white" hoverClass="hover:bg-gray-100" />

	<main class="max-w-md mx-auto px-6 sm:px-8 py-8 text-center">
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
				class="group inline-flex items-center justify-between w-48 sm:w-56 px-2 py-0 border border-black bg-white hover:bg-gray-50 transition-colors duration-300 shadow-[5px_5px_0px_0px_#B6531B,5px_5px_0px_1px_black]"
			>
				<span class="font-script text-black text-[16pt] sm:text-[20pt]">More info</span>
				<svg class="w-5 h-5 text-black group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
				</svg>
			</a>

			<a
				href="/rsvp"
				class="group inline-flex items-center justify-between w-48 sm:w-56 px-2 py-0 border border-black bg-white hover:bg-gray-50 transition-colors duration-300 shadow-[5px_5px_0px_0px_#B6531B,5px_5px_0px_1px_black]"
			>
				<span class="font-script text-black text-[16pt] sm:text-[20pt]">Pre RSVP</span>
				<svg class="w-5 h-5 text-black group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
					<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
				</svg>
			</a>
		</div>
	</main>
</div>
