<script>
	export let url = '#'; // The URL to navigate to
	export let label = ''; // The button text
	export let imgSrc = ''; // Optional image source
	export let imgAlt = ''; // Optional image alt text
	export let classes = ''; // Additional custom classes for styling
</script>

<button
	on:click={() => (window.location.href = url)}
	class={`inline-flex items-center p-2 bg-blue-500 text-white rounded hover:bg-blue-600 ${classes}`}
>
	{#if imgSrc}
		<img src={imgSrc} alt={imgAlt} class="w-5 h-5 rounded-full flex-shrink-0" />
	{/if}
	<span class="whitespace-nowrap pr-4 pl-1">{label}</span>
</button>
