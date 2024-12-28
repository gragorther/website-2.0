<script>
	import ClickableButton from '$lib/ClickableButton.svelte';
	import DualImage from '$lib/DualImage.svelte';
	import PageTitle from '$lib/PageTitle.svelte';
</script>

<PageTitle title="Links" />
<h2>Contact</h2>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li>
			<ClickableButton href="https://matrix.to/#/@gregor:gregtech.eu"
				><DualImage imgSrc="/matrix.svg">Matrix</DualImage></ClickableButton
			>
		</li>
		<li>
			<ClickableButton href="https://threema.id/6CH24JJE"
				><DualImage imgSrc="/threema.jpg">Threema</DualImage></ClickableButton
			>
		</li>
		<li>
			<ClickableButton href="mailto:gregor@gregtech.eu"
				><DualImage imgSrc="/email.svg">E-mail</DualImage></ClickableButton
			>
		</li>
	</div>
</ul>
<h2>Social media</h2>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li>
			<ClickableButton href="https://gregtech.eu/u/gregor"
				><DualImage imgSrc="/lemmy.png">Lemmy</DualImage></ClickableButton
			>
		</li>
		<li>
			<ClickableButton href="https://toot.si/@gregortactac"
				><DualImage imgSrc="/mastodon.svg">Mastodon</DualImage></ClickableButton
			>
		</li>
	</div>
</ul>
