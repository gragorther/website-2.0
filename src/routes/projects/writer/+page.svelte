<script lang="ts">
	import PageTitle from '$lib/PageTitle.svelte';
	import ResultBox from '$lib/ResultBox.svelte';
	let text: string = '';
	let maxlength = 300;
	import crypto from 'crypto';
	//const randomString = crypto.randomBytes(1).toString('hex');
	function color() {
		return '#' + ((Math.random() * 0xffffff) << 0).toString(16).padStart(6, '0');
	}
</script>

<PageTitle title="Writer" />
<div class=" overflow-auto p-4 flex flex-col text-black items-center justify-center">
	<textarea {maxlength} bind:value={text} class="w-1/2 border-2 p-2 border-violet-600 rounded-lg"
	></textarea>
	<div class="grid grid-cols-2 gap-4">
		<button class="pill-button" on:click={() => (text = text.toUpperCase())}>UPPER</button>
		<button class="pill-button" on:click={() => (text = text.toLowerCase())}>lower</button>
		<p>{text.length}/{maxlength}</p>
	</div>
	<div class="flex flex-wrap w-1/2 border-2 m-2">
		{#each text.split(' ') as word}
			<span class="break-all" style="color:{color()}">{word}</span>
		{/each}
	</div>
</div>
