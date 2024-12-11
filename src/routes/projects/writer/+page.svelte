<script lang="ts">
	import PageTitle from '$lib/PageTitle.svelte';
	import { Copy } from 'lucide-svelte';
	let text: string = '';

	function color() {
		return '#' + ((Math.random() * 0xffffff) << 0).toString(16).padStart(6, '0');
	}
	let i;
	function firstLetterUppercase(input) {
		var res = '';
		for (var i = 0; i < input.length; i++) {
			// Make every first character uppercase and second character lowercase alternately
			res += i % 2 === 0 ? input.charAt(i).toUpperCase() : input.charAt(i).toLowerCase();
		}
		return res;
	}
	import { copy } from 'svelte-copy';
</script>

<PageTitle title="Writer" />
<div class=" overflow-auto p-4 flex flex-col text-black items-center justify-center">
	<textarea bind:value={text} class="w-1/2 border-2 p-2 border-violet-600 rounded-lg"></textarea>
	<div class="grid grid-cols-4 gap-4">
		<button class="pill-button" on:click={() => (text = firstLetterUppercase(text))}>MoCkIfY</button
		>
		<button class="pill-button" on:click={() => (text = text.toUpperCase())}>UPPER</button>
		<button class="pill-button" on:click={() => (text = text.toLowerCase())}>lower</button>
		<button class="pill-button flex" use:copy={text}>Copy text<Copy class="ml-2" /></button>
	</div>
	<div class="flex flex-wrap w-1/2 border-2 m-2">
		{#each text.split(' ') as word}
			<span class="break-all" style="color:{color()}">{word}</span>
		{/each}
	</div>
</div>
