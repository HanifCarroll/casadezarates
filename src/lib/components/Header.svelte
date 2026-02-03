<script lang="ts">
	import { goto } from '$app/navigation';
	import Logo from './Logo.svelte';

	interface Props {
		bgClass?: string;
		hoverClass?: string;
	}

	let { bgClass = 'bg-white', hoverClass = 'hover:bg-gray-100' }: Props = $props();

	function openMenu() {
		goto('/menu');
	}
</script>

<header class="sticky top-0 z-50 w-full p-6 flex items-start justify-between {bgClass}">
	<button onclick={openMenu} class="p-2 {hoverClass} rounded transition-colors">
		<svg class="w-6 h-6 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
			<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
		</svg>
	</button>
	<a href="/" aria-label="Back to landing page">
		<Logo />
	</a>
	<div class="w-10"></div><!-- Spacer for centering -->
</header>
