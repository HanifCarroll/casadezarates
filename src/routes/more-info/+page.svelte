<script lang="ts">
	import Header from '$lib/components/Header.svelte';
</script>

<svelte:head>
	<title>More Info | Markis + Olivia</title>
</svelte:head>

<div class="min-h-screen bg-rose flex flex-col">
	<Header bgClass="bg-rose" hoverClass="hover:bg-white/10" />

	<main class="max-w-md mx-auto px-6 sm:px-8 py-8 text-center">
		<!-- Airport -->
		<section class="mb-10">
			<h2 class="font-script text-[28pt] sm:text-[40pt] text-black mb-1">Airport:</h2>
			<p class="font-sans text-[14pt] sm:text-[20pt] text-black">Mexico City International Airport</p>
			<p class="font-sans text-[14pt] sm:text-[20pt] text-black">Benito Juarez</p>
		</section>

		<!-- Where to stay -->
		<section class="mb-10">
			<h2 class="font-script text-[28pt] sm:text-[40pt] text-black mb-1">Where to stay:</h2>
			<p class="font-sans text-[14pt] sm:text-[20pt] text-black">Roma Norte, Roma, La Condesa</p>
			<p class="font-sans text-[14pt] sm:text-[20pt] text-black">Juarez</p>
		</section>

		<!-- Check this out -->
		<section class="mb-12">
			<h2 class="font-script text-[28pt] sm:text-[40pt] text-black mb-4">Check this out:</h2>
			<div class="flex justify-center">
				<a
					href="https://www.indietraveller.co/where-to-stay-in-mexico-city/"
					target="_blank"
					rel="noopener"
					class="group inline-flex items-center gap-3 px-2 py-0 border border-black bg-white hover:bg-gray-50 transition-colors duration-300 shadow-[5px_5px_0px_0px_#B6531B,5px_5px_0px_1px_black]"
				>
					<span class="font-script text-black text-[16pt] sm:text-[20pt]">Travel</span>
					<svg class="w-5 h-5 text-black group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
					</svg>
				</a>
			</div>
		</section>
	</main>
</div>
