<script lang="ts">
	interface Props {
		imgSrc?: string; // Image source URL
		imgAlt?: string; // Alternate text for the images
		children?: any;
	}

	let { imgSrc = '', imgAlt = '', children }: Props = $props();
	const imgclass: string = 'object-cover h-5 w-5';
</script>

<div class="flex items-center justify-center gap-0">
	<!-- Left Image -->
	<img src={imgSrc} alt={imgAlt} class="ml-1 {imgclass}" />
	{@render children?.()}
	<!-- Right Image -->
	<img src={imgSrc} alt={imgAlt} class="mr-1 {imgclass}" />
</div>
