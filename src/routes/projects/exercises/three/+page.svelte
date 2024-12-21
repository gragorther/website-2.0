<script lang="ts">
	import { run } from 'svelte/legacy';

	import PageTitle from '$lib/PageTitle.svelte';

	/**
	 * Ustvarili bomo preprosto aplikacijo za seznam nakupov,
	 * kjer lahko dodajamo izdelke in njihove cene.
	 * Aplikacija bo samodejno izračunala skupno vsoto in prikazala število izdelkov.
	 *
	 * Vmesnik je sestavljen iz treh glavnih delov:
	 *  - Seznam obstoječih izdelkov
	 *  - Obrazec za dodajanje novih izdelkov
	 *  - Prikaz skupne vsote in števila izdelkov
	 *
	 * NALOGA:
	 *  - Dodaj obrazec za dodajanje novih izdelkov
	 *  - Dokončaj funkcijo addItem()
	 *  - Izračunaj skupno ceno izdelkov (total)
	 */

	// Najprej definirajmo tip podatkov za naše izdelke:
	type Item = {
		name: string;
		price: number;
	};
	// Priprava spremenljivk
	let items: Item[] = $state([{ name: 'Banana', price: 10 }]); // seznam vseh izdelkov
	let newItemName = $state(''); // ime novega izdelka
	let newItemPrice = $state(0); // cena novega izdelka

	// Ustvarimo funkcijo, ki bo dodajala nove izdelke v seznam:
	function add() {
		items = [
			...items,
			{
				name: newItemName,
				price: newItemPrice
			}
		];
		newItemPrice = 0;
		newItemName = '';
	}

	function sumItemsPrice(items: Item[]) {
		let sestevek = 0;
		items.forEach((i) => {
			console.log(i, i.price, typeof i.price);
			sestevek += i.price;
		});
		return sestevek;
	}

	let total = $state(0);
	run(() => {
		total = sumItemsPrice(items);
	});
</script>

<PageTitle title="Shopping list" />
{#each items as item}
	<div class="flex justify-between p-2 border-b border-gray-100">
		<span class="font-medium">{item.name}</span>
		<span class="text-gray-600">${item.price}</span>
	</div>
{/each}

<div class="justiy-center flex flex-col items-center">
	<div>
		<h2 class="text-2xl m-1">Item name</h2>
		<input type="text" bind:value={newItemName} class="rounded-full text-black p-2" />
	</div>
	<div>
		<h2 class="text-2xl m-1">Item price</h2>
		<input type="number" bind:value={newItemPrice} class="rounded-full text-black p-2" />
	</div>
	<div>
		<button class="pill-button" onclick={add}>Add</button>
	</div>
</div>

<div class="flex justify-between text-lg font-semibold border-t-2 mt-12 pt-4">
	<span>Total:</span>
	<span>${total}</span>
</div>
