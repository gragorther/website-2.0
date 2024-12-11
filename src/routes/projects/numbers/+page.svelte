<script lang="ts">
	import PageTitle from '$lib/PageTitle.svelte';
	import ResultBox from '$lib/ResultBox.svelte';
	let stevilo: number;
	let sodo: boolean;
	let vsota: number;
	let seznamDeliteljev: number[] = [];

	function jeSodo(num: number) {
		return num % 2 == 0;
	}

	function izpisiDeliteljev(num: number) {
		let delitelji: number[] = [];

		for (let i = 1; i < num; i++) {
			if (num % i == 0) {
				delitelji.push(i);
			}
		}
		return delitelji;
	}
	function vsotaDeliteljev(nums: number[]) {
		let sestevek = 0;
		for (const i of nums) {
			sestevek += i;
		}
		return sestevek;
	}
	$: {
		sodo = jeSodo(stevilo);
		seznamDeliteljev = izpisiDeliteljev(stevilo);
		vsota = vsotaDeliteljev(seznamDeliteljev);
	}
</script>

<PageTitle title="Števila" />
<div class="flex flex-col justify-center gap-2 items-center min-h-screen text-center">
	<input
		class="border-2 text-black border-pink-400 rounded-full text-center p-4 text-4xl"
		bind:value={stevilo}
	/>
	<div class="flex flex-row gap-4 flex-wrap justify-center items-start text-center">
		<ResultBox>
			<p>Število je:</p>
			<p>{sodo ? 'sodo' : 'liho'}</p>
		</ResultBox>
		<ResultBox>
			<p>Seznam deliteljev:</p>
			<div class="flex flex-wrap gap-1">
				{#each seznamDeliteljev as st}
					<span class="bg-pink-200 text-pink-800 rounded text-sm">{st}</span>
				{/each}
			</div>
		</ResultBox>
		<ResultBox>
			<p>Vsota deliteljev je: {vsota}</p>
		</ResultBox>
	</div>
</div>
