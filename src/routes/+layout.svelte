<script lang="ts">
	import { injectAnalytics } from '@vercel/analytics/sveltekit';
	injectAnalytics();
	import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';
	injectSpeedInsights();
	import '../app.css';
	let navclass;
	navclass =
		'rounded-lg bg-purple-400 text-2xl flex-grow text-center mr-2 hover:bg-purple-700 text-white hover:text-white';
</script>

<nav class="rounded-lg m-4">
	<div class="content-center flex justify-evenly">
		<a href="/" class={navclass}>Home</a>
		<a href="/contact" class={navclass}>Contact</a>
		<a href="/gallery" class={navclass}>Gallery</a>
		<a href="/blog" class={navclass}>Blog</a>
		<a href="/donations" class={navclass}>Donations</a>
	</div>
</nav>
<slot />

<style lang="postcss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;

	@layer base {
		.shared-properties {
			@apply bg-gradient-to-r  text-transparent bg-clip-text font-extrabold mx-auto my-5 text-center leading-relaxed;
		}
	}
	:global(body) {
		@apply bg-zinc-900;
	}
	:global(*) {
		@apply text-white;
	}

	:global(p) {
		@apply text-lg;
		@apply my-3;
		@apply mx-40;
	}
	:global(h1) {
		@apply shared-properties text-6xl  from-pink-500 to-violet-500 leading-relaxed;
	}
	:global(a) {
		@apply text-lg;
		@apply text-blue-400 hover:text-blue-200;
	}
	:global(h2) {
		@apply shared-properties text-4xl from-blue-500 to-pink-700;
	}
	/*:global(li) {
		@apply border border-lime-400 rounded-lg font-extrabold rounded-full;
	}*/
	:global(button) {
		@apply rounded-full bg-purple-400 p-5 text-white hover:text-white;
	}
	:global(.pill-button) {
		@apply text-white hover:text-white bg-purple-400 rounded-full px-4 py-2 hover:bg-purple-500;
	}
	:global(ul) {
		@apply flex items-center justify-center;
	}
</style>
