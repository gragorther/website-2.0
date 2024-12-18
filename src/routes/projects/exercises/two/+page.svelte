<script lang="ts">
	/**
	 * NALOGA:
	 * - Poglej v data.ts; tam bos nasel seznam categories (ki je tu ze importan)
	 * - V grid-u s tremi stolpci prikazi vse kategorije s karticami (uporabi komponento Card)
	 * - Vsaka kartica naj ima: Naslov, Opis, Sliko
	 *
	 * DODATNA NALOGA:
	 * - Na telefonu (oz majhnem ekranu) naj se kartice prikazejo v 1 stolpcu
	 *  (Pomoč: https://tailwindcss.com/docs/responsive-design)
	 */

	import { categories } from './data';
	import Card from './Card.svelte';
	import ColorChangingTitle from '$lib/ColorChangingTitle.svelte';
</script>

<div class="flex flex-wrap justify-center gap-1">
	{#each categories as category}
		<Card {category} />
	{/each}
</div>
