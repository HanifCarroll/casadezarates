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

<main class="min-h-screen bg-terracotta flex flex-col items-center justify-center p-8">
	<div class="flex-1 flex items-center justify-center">
		<img
			src="/LandingPage.gif"
			alt="Markis + Olivia"
			class="max-w-full max-h-[60vh] object-contain"
		/>
	</div>

	<div class="pb-16">
		<button
			onclick={handleSaveTheDate}
			class="group flex items-center gap-3 px-6 py-3 border border-black bg-white hover:bg-gray-50 transition-colors duration-300 cursor-pointer shadow-[5px_5px_0px_0px_#CD8789,5px_5px_0px_1px_black]"
		>
			<span class="text-black font-script text-[26pt]">Save the date</span>
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
