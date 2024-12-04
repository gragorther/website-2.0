<script>
	import ClickableButton from '$lib/ClickableButton.svelte';
</script>

<h1>My projects</h1>
<p>Stuff I made at a coding class</p>
<ul>
	<li>
		<ClickableButton url="/projects/to-do" label="To-do list" />
	</li>
	<li>
		<ClickableButton url="/projects/numbers" label="Info about a number" />
	</li>
	<li>
		<ClickableButton url="/projects/tvitr" label="Tvitr"></ClickableButton>
	</li>
</ul>
