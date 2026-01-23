<script lang="ts">
	import { goto } from '$app/navigation';

	function handleSaveTheDate() {
		goto('/save-the-date');
	}
</script>

<svelte:head>
	<title>Markis + Olivia | Casa de Zarates</title>
	<meta name="description" content="Save the date for Markis and Olivia's wedding in Mexico City" />
</svelte:head>

<main class="h-dvh bg-terracotta flex flex-col items-center justify-center gap-6 sm:gap-10 p-4 sm:p-8">
	<div class="flex items-center justify-center w-full">
		<img
			src="/LandingPage.gif"
			alt="Markis + Olivia"
			class="max-w-[85%] sm:max-w-full max-h-[65vh] object-contain"
		/>
	</div>

	<div class="">
		<button
			onclick={handleSaveTheDate}
			class="group flex items-center gap-3 px-4 py-2 border border-black bg-white hover:bg-gray-50 transition-colors duration-300 cursor-pointer shadow-[5px_5px_0px_0px_#CD8789,5px_5px_0px_1px_black]"
		>
			<span class="text-black font-script text-[20pt] sm:text-[26pt]">Save the date</span>
			<svg
				class="w-5 h-5 text-black group-hover:translate-x-1 transition-transform duration-300"
				fill="none"
				stroke="currentColor"
				viewBox="0 0 24 24"
			>
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
			</svg>
		</button>
	</div>
</main>
