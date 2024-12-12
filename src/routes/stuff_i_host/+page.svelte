<script>
	import ClickableButton from '$lib/ClickableButton.svelte';
	import PageTitle from '$lib/PageTitle.svelte';
</script>

<PageTitle title="Stuff I host" />
<h2>Zero-contact registration</h2>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li>
			<ClickableButton
				url="https://gregtech.eu"
				label="Lemmy"
				imgSrc="lemmy.svg"
				imgAlt="Lemmy logo"
			/>
		</li>
		<li>
			<ClickableButton
				url="https://search.gregtech.eu"
				label="SearXNG"
				imgSrc="searxng-wordmark.svg"
				imgAlt="SearXNG logo"
			/>
		</li>
	</div>
</ul>
<h2>Contact me for registration on these</h2>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li>
			<ClickableButton
				url="https://vaultwarden.gregtech.eu"
				label="Vaultwarden"
				imgSrc="vaultwarden.png"
				imgAlt="Vaultwarden logo"
			/>
		</li>
		<li>
			<ClickableButton
				url="https://app.element.io"
				label="Matrix"
				imgSrc="matrix.svg"
				imgAlt="Matrix logo"
			/>
		</li>
	</div>
</ul>
