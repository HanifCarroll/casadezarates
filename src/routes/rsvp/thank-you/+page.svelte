<script lang="ts">
	import { goto } from '$app/navigation';

	function openMenu() {
		goto('/menu');
	}
</script>

<svelte:head>
	<title>Thank You | Markis + Olivia</title>
</svelte:head>

<main class="min-h-screen bg-gold flex flex-col">
	<!-- Header with hamburger menu and logo - STICKY -->
	<header class="fixed top-0 left-0 right-0 z-50 bg-gold p-6 flex items-start justify-between">
		<button onclick={openMenu} class="p-2 hover:bg-black/10 rounded transition-colors">
			<svg class="w-6 h-6 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
			</svg>
		</button>
		<div class="font-script text-2xl text-black text-center leading-tight">
			M<br />+<br />O
		</div>
		<div class="w-10"></div>
	</header>

	<!-- Content - with padding for fixed header -->
	<div class="flex-1 flex items-center justify-center pt-32 px-6">
		<h1 class="font-script text-[28pt] sm:text-[40pt] text-black">Thank you :)</h1>
	</div>
</main>
