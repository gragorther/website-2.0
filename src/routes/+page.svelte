<script>
	import ClickableButton from '$lib/ClickableButton.svelte';
	import DualImage from '$lib/DualImage.svelte';
	import PageTitle from '$lib/PageTitle.svelte';
</script>

<PageTitle title="GregTech" />
<p>
	I'm an enjoyer of FOSS, especially Linux. I like gaming a lot. I play Minecraft, CS2, Scarlet
	Hollow, which I speedran in a day and a whole lot of other games. All of these games, with the
	exception of Minecraft, I got through Steam. I'm from Slovenia, which is a small country in
	central Europe.
</p>
<p>
	<a href="gregtech.eu">gregtech.eu</a> is my own Lemmy server, and also a Matrix server. If you'd like
	an account on Lemmy, you can do so without my permission, but for Matrix you would have to contact
	me. I host it all at Hetzner in Helsinki, but my Minecraft server is hosted on a Raspberry Pi at home.
</p>
<h2>Other cool websites</h2>
<ul>
	<li>
		<ClickableButton href="https://tsugu.xyz"
			><DualImage imgSrc="/tsugulogo.png" imgAlt="Tsugu logo">Tsugu</DualImage></ClickableButton
		>
	</li>
	<li>
		<ClickableButton href="https://suricrasia.online/iceberg/"
			><DualImage imgSrc="/suricrasia.png">Programming iceberg</DualImage></ClickableButton
		>
	</li>
	<li>
		<ClickableButton href="https://landchad.net/"
			><DualImage imgSrc="/landchad.png">Landchad</DualImage></ClickableButton
		>
	</li>
	<li>
		<ClickableButton href="https://popey.com/blog/"
			><DualImage imgSrc="/popey.ico">Popey blog</DualImage></ClickableButton
		>
	</li>
</ul>
