<script>
	import ClickableButton from '$lib/ClickableButton.svelte';
	import PageTitle from '$lib/PageTitle.svelte';
</script>

<PageTitle title="Links" />
<h2>Contact</h2>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li>
			<ClickableButton
				url="https://matrix.to/#/@gregor:gregtech.eu"
				label="Matrix"
				imgSrc="matrix.svg"
				imgAlt="Matrix logo"
			/>
		</li>
		<li>
			<ClickableButton
				url="https://threema.id/6CH24JJE"
				label="Threema"
				imgSrc="threema.jpg"
				imgAlt="Threema logo"
			/>
		</li>
		<li>
			<ClickableButton
				url="mailto:gregor@gregtech.eu"
				label="E-mail"
				imgSrc="email.png"
				imgAlt="E-mail logo"
			/>
		</li>
	</div>
</ul>
<h2>Social media</h2>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li>
			<ClickableButton
				url="https://gregtech.eu/u/gregor"
				label="Lemmy"
				imgSrc="lemmy.png"
				imgAlt="Lemmy logo"
			/>
		</li>
		<li>
			<ClickableButton
				url="https://toot.si/@gregortactac"
				label="Mastodon"
				imgSrc="Mastodon_logotype_(simple)_new_hue.svg"
				imgAlt="Mastodon logo"
			/>
		</li>
	</div>
</ul>
