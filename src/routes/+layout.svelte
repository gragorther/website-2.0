<script lang="ts">
	import '../app.css';
	let navclass;
	navclass =
		'border border-emerald-500 border-2 rounded-lg bg-purple-400 text-2xl flex-grow text-center mr-2 hover:bg-red-400';
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
</style>
