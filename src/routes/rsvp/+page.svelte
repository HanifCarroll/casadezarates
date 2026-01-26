<script lang="ts">
	import { goto } from '$app/navigation';
	import Logo from '$lib/components/Logo.svelte';

	let fullName = $state('');
	let status = $state('');

	const GOOGLE_FORM_URL = 'https://docs.google.com/forms/d/e/1FAIpQLSdLLPc2n1U23l0My_GlyNX-Uyyxx8810_lmR5ll63tkbFaYVA/formResponse';
	const ENTRY_NAME = 'entry.1881324885';
	const ENTRY_STATUS = 'entry.662734428';

	// Map our status values to Google Form values
	const statusMap: Record<string, string> = {
		accepting: 'Joyfully accepting',
		hoping: 'Hoping to make it, TBD',
		declining: "Sadly, can't make it"
	};

	function openMenu() {
		goto('/menu');
	}

	async function handleSubmit(e: Event) {
		e.preventDefault();

		const formData = new FormData();
		formData.append(ENTRY_NAME, fullName);
		formData.append(ENTRY_STATUS, statusMap[status] || status);

		try {
			// Submit to Google Forms (no-cors because Google doesn't allow CORS)
			await fetch(GOOGLE_FORM_URL, {
				method: 'POST',
				mode: 'no-cors',
				body: formData
			});
		} catch (error) {
			// Even if there's an error, the data is usually submitted
			console.log('Form submitted');
		}

		goto('/rsvp/thank-you');
	}
</script>

<svelte:head>
	<title>Pre RSVP | Markis + Olivia</title>
</svelte:head>

<main class="min-h-screen bg-gold flex flex-col">
	<!-- Header with hamburger menu and logo - STICKY -->
	<header class="fixed top-0 left-0 right-0 z-50 bg-gold p-6 flex items-start justify-between">
		<button onclick={openMenu} class="p-2 hover:bg-black/10 rounded transition-colors">
			<svg class="w-6 h-6 text-black" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
			</svg>
		</button>
		<Logo />
		<div class="w-10"></div>
	</header>

	<!-- Content - with padding for fixed header -->
	<div class="flex-1 max-w-md mx-auto px-6 sm:px-8 w-full pt-36">
		<!-- Disclaimer -->
		<p class="font-mono text-[12pt] sm:text-[14pt] text-black text-center mb-8 leading-relaxed">
			*This is not an official RSVP.<br />
			Just a "giving us a heads up".<br />
			Formal RSVP shall come later :)
		</p>

		<form onsubmit={handleSubmit} class="space-y-8">
			<!-- Full Name -->
			<div class="text-center">
				<label for="fullName" class="font-script text-[28pt] sm:text-[40pt] text-black block mb-2">Full Name:</label>
				<input
					type="text"
					id="fullName"
					bind:value={fullName}
					required
					class="w-full max-w-xs mx-auto block border-2 border-black bg-white px-2 py-0 font-mono text-[14pt] sm:text-[16pt] text-black focus:outline-none focus:ring-2 focus:ring-black"
				/>
			</div>

			<!-- Status -->
			<div class="text-center">
				<p class="font-script text-[28pt] sm:text-[40pt] text-black mb-4">Status:</p>
				<div class="space-y-4 text-left max-w-xs mx-auto">
					<label class="flex items-start gap-3 cursor-pointer">
						<input
							type="radio"
							name="status"
							value="accepting"
							bind:group={status}
							class="mt-1 w-5 h-5 border-2 border-black bg-white appearance-none checked:bg-black"
						/>
						<span class="font-mono text-[12pt] sm:text-[14pt] text-black leading-tight">
							Joyfully accepting,<br />save me a seat.
						</span>
					</label>

					<label class="flex items-start gap-3 cursor-pointer">
						<input
							type="radio"
							name="status"
							value="hoping"
							bind:group={status}
							class="mt-1 w-5 h-5 border-2 border-black bg-white appearance-none checked:bg-black"
						/>
						<span class="font-mono text-[12pt] sm:text-[14pt] text-black">
							Hoping to make it, TBD
						</span>
					</label>

					<label class="flex items-start gap-3 cursor-pointer">
						<input
							type="radio"
							name="status"
							value="declining"
							bind:group={status}
							class="mt-1 w-5 h-5 border-2 border-black bg-white appearance-none checked:bg-black"
						/>
						<span class="font-mono text-[12pt] sm:text-[14pt] text-black leading-tight">
							Sadly, can't make it.<br />Celebrating from a far
						</span>
					</label>
				</div>
			</div>

			<!-- Submit button (hidden, form submits on selection) -->
			<div class="text-center pt-4">
				<button
					type="submit"
					class="font-script text-[16pt] sm:text-[20pt] text-black px-2 py-0 border border-black bg-white hover:bg-gray-50 transition-colors shadow-[5px_5px_0px_0px_#B6531B,5px_5px_0px_1px_black]"
				>
					Submit
				</button>
			</div>
		</form>
	</div>
</main>
