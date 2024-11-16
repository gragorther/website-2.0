<script>
	import ClickableButton from '$lib/ClickableButton.svelte';
</script>

<h1>Links</h1>
<h2>Contact</h2>
<ul>
	<li>
		<ClickableButton
			url="https://matrix.to/#/@gregor:gregtech.eu"
			label="Matrix"
			imgSrc="element.svg"
			imgAlt="Element logo"
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
</ul>
