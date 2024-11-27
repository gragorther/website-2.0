<script lang="ts">
	import ResultBox from '$lib/ResultBox.svelte';
	import AppBox from '$lib/ResultBox.svelte';
	let stevilo = 3;
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

<h1>Števila</h1>
<div class="flex"></div>
<div class="flex flex-col justify-center gap-2 items-center min-h-screen">
	<input
		class="border-2 text-black border-pink-400 rounded-full text-center p-4 text-4xl"
		bind:value={stevilo}
	/>
	<div class="flex flex-row">
		<ResultBox>
			<p>Število je:</p>
			<p>{sodo ? 'sodo' : 'liho'}</p>
		</ResultBox>
		<ResultBox>
			<p>Seznam deliteljev:</p>
			<ul>
				{#each seznamDeliteljev as st}
					<li>{st}</li>
				{/each}
			</ul>
		</ResultBox>
		<ResultBox>
			<p>Vsota deliteljev je: {vsota}</p>
		</ResultBox>
	</div>
</div>
