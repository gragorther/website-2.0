<script lang="ts">
	import type { UserPost } from '$lib';
	import PageTitle from '$lib/PageTitle.svelte';
	import Post from '$lib/Post.svelte';

	let posts: UserPost[] = $state([]);
	let newPost: string = $state('');
	function add() {
		posts = [
			{
				text: newPost,
				timestamp: Date.now(),
				likes: 0
			},
			...posts
		];
		newPost = '';
	}
</script>

<PageTitle title="Tvitr" />
<div class="justify-center flex pb-3">
	<input type="text" bind:value={newPost} class="rounded-full text-black p-2" />
	<button class="pill-button" onclick={add}>Post</button>
</div>
<div class="flex flex-wrap">
	{#each posts as post}
		<Post {post} />
	{/each}
</div>
