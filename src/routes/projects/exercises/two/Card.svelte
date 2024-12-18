<script lang="ts">
	import type { Category } from './data';

	export let category: Category;
</script>

<div class="border-2 border-pink-400 rounded-2xl max-w-xs overflow-auto">
	<div class="flex flex-col items-center text-center">
		<h1 class="break-all">{category.name}</h1>
		<img class=" rounded-lg" src={category.image} alt="Category" />
		<p class="p-1 m-1 pb-3">{category.description}</p>
	</div>
</div>
