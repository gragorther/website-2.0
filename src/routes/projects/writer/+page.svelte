<script lang="ts">
	import PageTitle from '$lib/PageTitle.svelte';
	import { Copy } from 'lucide-svelte';
	let text: string = $state('');

	let i;
	function firstLetterUppercase(input: string) {
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
<div class=" overflow-x-hidden p-4 flex flex-col text-black items-center justify-center">
	<textarea bind:value={text} class="w-1/2 border-2 p-2 border-violet-600 rounded-lg"></textarea>
	<div class="flex flex-wrap gap-2 justify-center">
		<button class="pill-button" onclick={() => (text = firstLetterUppercase(text))}>MoCkIfY</button>
		<button class="pill-button" onclick={() => (text = text.toUpperCase())}>UPPER</button>
		<button class="pill-button" onclick={() => (text = text.toLowerCase())}>lower</button>
		<button class="pill-button flex" use:copy={text}>Copy text<Copy class="ml-2" /></button>
	</div>
</div>
