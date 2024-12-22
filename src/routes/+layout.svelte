<script lang="ts">
	import { injectAnalytics } from '@vercel/analytics/sveltekit';
	injectAnalytics();
	import { injectSpeedInsights } from '@vercel/speed-insights/sveltekit';
	injectSpeedInsights();
	import '../app.css';
	import ResultBox from '$lib/ResultBox.svelte';
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();

	let navclass =
		'rounded-lg bg-purple-400 text-xl p-2 text-center hover:bg-purple-700 text-white flex-grow mr-2 sm:text-lg sm:p-3 lg:text-xl lg:p-0 ';
</script>

<nav class="rounded-lg m-4">
	<!-- Use flex-wrap to handle wrapping on smaller screens -->
	<div class="content-center flex flex-wrap justify-evenly gap-2">
		<a href="/" class={navclass}>Home</a>
		<a href="/contact" class={navclass}>Contact</a>
		<a href="/gallery" class={navclass}>Gallery</a>
		<a href="/blog" class={navclass}>Blog</a>
		<a href="/stuff_i_host" class={navclass}>Stuff I host</a>
		<a href="/projects" class={navclass}>Projects</a>
	</div>
</nav>
<div class="min-h-screen flex flex-col pb-16">
	<main class="flex-grow">
		{@render children?.()}
	</main>
	<div class="flex justify-center text-sm pb-8 mt-2">
		<ResultBox>
			The source code for this website is available on
			<a
				href="https://github.com/gragorther/website-2.0"
				class="text-white hover:text-white bg-purple-400 text-sm rounded-full p-1 hover:bg-purple-500"
				>my GitHub page</a
			>
		</ResultBox>
	</div>
</div>

<style lang="postcss">
	@tailwind base;

	@layer base {
		.shared-properties {
			@apply bg-gradient-to-r text-transparent bg-clip-text font-extrabold mx-auto my-5 text-center p-2;
		}
	}
	:global(body) {
		@apply bg-zinc-900 text-white font-mono text-center;
	}
	/* :global(*) {
		@apply text-white;
	} */

	:global(p) {
		@apply text-lg my-3 mx-4 lg:mx-40 text-left; /* Add smaller margins on mobile */
	}
	:global(h1) {
		@apply shared-properties text-4xl lg:text-6xl from-pink-500 to-violet-500 leading-relaxed;
	}
	:global(a) {
		@apply text-lg lg:text-xl text-blue-600 hover:text-blue-400;
	}
	:global(h2) {
		@apply shared-properties text-3xl lg:text-4xl from-orange-500 to-pink-700 leading-relaxed;
	}

	/* Buttons and navigation */
	:global(.pill-button) {
		@apply text-white hover:text-white bg-purple-400 rounded-full px-4 py-2 mt-2 hover:bg-purple-500;
	}

	/* Responsive navigation layout */
	:global(ul) {
		@apply flex flex-row items-center justify-center;
	}

	/* Make navigation adapt to smaller screens */

	:global(li) {
		@apply mx-4 text-lg;
	}
</style>
