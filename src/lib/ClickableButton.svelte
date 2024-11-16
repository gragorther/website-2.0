<script>
	export let url = '#'; // The URL to navigate to
	export let label = ''; // The button text
	export let imgSrc = ''; // Optional image source
	export let imgAlt = ''; // Optional image alt text
	export let classes = ''; // Additional custom classes for styling
</script>

<button
	on:click={() => (window.location.href = url)}
	class={`flex items-center space-x-2 p-2 bg-blue-500 text-white rounded hover:bg-blue-600${classes} m-3`}
>
	{#if imgSrc}
		<img src={imgSrc} alt={imgAlt} class="w-5 h-5 rounded-full" />
	{/if}
	<span>{label}</span>
</button>

<style>
	/* Add any additional scoped styles here if needed */
</style>
