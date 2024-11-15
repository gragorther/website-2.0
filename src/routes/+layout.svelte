<script lang="ts">
	import { injectAnalytics } from '@vercel/analytics/sveltekit';
	injectAnalytics();
	import '../app.css';
	let navclass;
	navclass =
		'border border-emerald-500 border-2 rounded-lg bg-purple-400 text-2xl flex-grow text-center mr-2 hover:bg-red-400 ';
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
	:global(body) {
		@apply bg-zinc-900;
	}
	:global(*) {
		@apply text-white;
		@apply overflow-x-hidden;
	}
	:global(p) {
		@apply text-white;
		@apply text-lg;
		@apply m-3;
	}
</style>
