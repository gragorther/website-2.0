<script lang="ts">
	interface Props {
		url?: string; // The URL to navigate to
		label?: string; // The button text
		imgSrc?: string; // Optional image source
		imgAlt?: string; // Optional image alt text
		classes?: string; // Additional custom classes for styling
	}

	let {
		url = '#',
		label = '',
		imgSrc = '',
		imgAlt = '',
		classes = ''
	}: Props = $props();
</script>

<button
	onclick={() => (window.location.href = url)}
	class={`inline-flex items-center p-2 pr-3 sm:pr-0 bg-blue-500 text-white rounded hover:bg-blue-600 ${classes}`}
>
	{#if imgSrc}
		<img src={imgSrc} alt={imgAlt} class="w-5 h-5 flex-shrink-0" />
	{/if}
	<span class="whitespace-nowrap pr-4 pl-1">{label}</span>
</button>
