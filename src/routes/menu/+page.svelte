<script lang="ts">
	import { goto } from '$app/navigation';

	function closeMenu() {
		history.back();
	}
</script>

<svelte:head>
	<title>Menu | Markis + Olivia</title>
</svelte:head>

<main class="h-dvh max-h-dvh bg-brown flex flex-col p-6 sm:p-8 overflow-hidden">
	<!-- Close button -->
	<button onclick={closeMenu} class="self-start p-2 hover:bg-white/10 rounded transition-colors">
		<svg class="w-6 h-6 sm:w-8 sm:h-8 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
			<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
		</svg>
	</button>

	<!-- Menu items -->
	<nav class="flex-1 flex flex-col justify-center items-center space-y-3 sm:space-y-8">
		<a href="/" class="font-script text-[26pt] sm:text-[49pt] text-white hover:opacity-80 transition-opacity">
			Home
		</a>
		<a href="/save-the-date" class="font-script text-[26pt] sm:text-[49pt] text-white hover:opacity-80 transition-opacity">
			Save the Date
		</a>
		<a href="/more-info" class="font-script text-[26pt] sm:text-[49pt] text-white hover:opacity-80 transition-opacity">
			More info
		</a>
		<a href="/rsvp" class="font-script text-[26pt] sm:text-[49pt] text-white hover:opacity-80 transition-opacity">
			Pre RSVP
		</a>
	</nav>
</main>
