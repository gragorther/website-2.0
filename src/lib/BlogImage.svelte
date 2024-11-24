<script lang="ts">
	export let src: string = ''; // The image source
	export let alt: string = ''; // Alternative text for the image
	export let maxWidth: string = '800px'; // Optional maximum width for the image
</script>

<div class="flex justify-center items-center my-4">
	<img
		{src}
		{alt}
		class="rounded-lg shadow-lg w-full max-w-full object-contain"
		style={`max-width: ${maxWidth};`}
		loading="lazy"
	/>
</div>
