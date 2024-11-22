<script lang="ts">
	import { injectAnalytics } from '@vercel/analytics/sveltekit';
	injectAnalytics();
	import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';
	injectSpeedInsights();
	import '../app.css';

	let navclass =
		'rounded-lg bg-purple-400 text-lg lg:text-2xl flex-grow text-center mr-2 hover:bg-purple-700 text-white hover:text-white p-2';
</script>

<nav class="rounded-lg m-4">
	<!-- Use flex-wrap to handle wrapping on smaller screens -->
	<div class="content-center flex flex-wrap justify-evenly gap-2">
		<a href="/" class={navclass}>Home</a>
		<a href="/contact" class={navclass}>Contact</a>
		<a href="/gallery" class={navclass}>Gallery</a>
		<a href="/blog" class={navclass}>Blog</a>
		<a href="/donations" class={navclass}>Donations</a>
		<a href="/stuff_i_host" class={navclass}>Stuff I host</a>
	</div>
</nav>
<div class="min-h-screen flex flex-col">
	<main class="flex-grow pb-10">
		<slot />
	</main>
</div>

<style lang="postcss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;

	@layer base {
		.shared-properties {
			@apply bg-gradient-to-r text-transparent bg-clip-text font-extrabold mx-auto my-5 text-center;
		}
	}
	:global(body) {
		@apply bg-zinc-900;
	}
	:global(*) {
		@apply text-white;
	}

	:global(p) {
		@apply text-lg my-3 mx-4 lg:mx-40; /* Add smaller margins on mobile */
	}
	:global(h1) {
		@apply shared-properties text-4xl lg:text-6xl from-pink-500 to-violet-500 leading-relaxed;
	}
	:global(a) {
		@apply text-lg lg:text-xl text-blue-400 hover:text-blue-200;
	}
	:global(h2) {
		@apply shared-properties text-3xl lg:text-4xl from-orange-500 to-pink-700 leading-relaxed;
	}

	/* Buttons and navigation */
	:global(.pill-button) {
		@apply text-white hover:text-white bg-purple-400 rounded-full px-4 py-2 hover:bg-purple-500;
	}

	/* Responsive navigation layout */
	:global(ul) {
		@apply flex flex-row items-center justify-center;
	}

	/* Make navigation adapt to smaller screens */
	:global(nav div) {
		@apply flex flex-wrap gap-2; /* Allow wrapping and spacing for smaller screens */
	}
</style>
