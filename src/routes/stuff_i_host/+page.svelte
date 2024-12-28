<script>
	import ClickableButton from '$lib/ClickableButton.svelte';
	import DualImage from '$lib/DualImage.svelte';
	import PageTitle from '$lib/PageTitle.svelte';
</script>

<PageTitle title="Stuff I host" />
<h2>Zero-contact registration</h2>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li>
			<ClickableButton href="https://gregtech.eu"
				><DualImage imgSrc="/lemmy.png">Lemmy</DualImage></ClickableButton
			>
		</li>
		<li>
			<ClickableButton href="https://search.gregtech.eu"
				><DualImage imgSrc="/searxng-wordmark.svg">SearXNG</DualImage></ClickableButton
			>
		</li>
	</div>
</ul>
<h2>Contact me for registration on these</h2>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li>
			<ClickableButton href="https://vaultwarden.gregtech.eu"
				><DualImage imgSrc="/vaultwarden.png">Vaultwarden</DualImage></ClickableButton
			>
		</li>
		<li>
			<ClickableButton href="https://app.element.io"
				><DualImage imgSrc="/matrix.svg">Matrix</DualImage></ClickableButton
			>
		</li>
	</div>
</ul>
