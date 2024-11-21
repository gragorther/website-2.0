<script lang="ts">
	export let images: { src: string; alt: string }[] = [];
	export let columns: number = 3;
	export let gap: string = '1rem';
</script>

<div class="grid" style="grid-template-columns: repeat({columns}, 1fr); gap: {gap};">
	{#each images as { src, alt }}
		<div class="image-container">
			<a href={src} target="_blank" rel="noopener noreferrer">
				<img {src} {alt} class="rounded-md shadow-md cursor-pointer" loading="lazy" />
			</a>
			<div class="description-box">
				<p class="description-text">{alt}</p>
			</div>
		</div>
	{/each}
</div>

<style>
	/* Grid layout for images */
	.grid {
		display: grid;
	}

	.image-container {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	/* Description box below images */
	.description-box {
		margin-top: 0.5rem;
		padding: 0.5rem;
		background: rgba(255, 255, 255, 0.1);
		border-radius: 0.25rem;
		box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
		text-align: center;
		width: 100%;
	}

	.description-text {
		font-size: 0.875rem;
		color: #fff;
	}

	/* Styling for images */
	img {
		border-radius: 0.5rem;
		box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
		width: 100%;
		transition: transform 0.2s ease;
	}

	img:hover {
		transform: scale(1.05);
	}
</style>
