<script lang="ts">
	import Blog from '$lib/Blog.svelte';
	import PageTitle from '$lib/PageTitle.svelte';

	const posts = [
		{
			link: '/blog/posts/ImmutableDistros',
			image: 'fedora-silverblue-dark.png',
			title: 'Immutable Linux Distributions',
			previewText:
				"In immutable distros, you can't modify the root partition of your operating system, which provides protection against accidentally bricking your operating system."
		},
		{
			link: '/blog/posts/EUChatControl',
			image: 'regain_privacy_threema_sticker.jpg',
			title: 'Chat control, the privacy nightmare that keeps coming back',
			previewText:
				'I am a 13-year-old student from Slovenia. I care about privacy and my future as an EU citizen, and currently the future is looking bleak'
		}
	];
</script>

<PageTitle title="Blog" />
<div class="flex flex-wrap gap-6 justify-center">
	{#each posts as post}
		<Blog link={post.link} image={post.image} title={post.title} previewText={post.previewText} />
	{/each}
</div>
