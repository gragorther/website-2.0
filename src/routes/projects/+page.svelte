<script>
	import ClickableButton from '$lib/ClickableButton.svelte';
	import PageTitle from '$lib/PageTitle.svelte';
</script>

<PageTitle title="Projects" />
<p class="text-center">Stuff I made at a coding class</p>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li><ClickableButton url="/projects/writer" label="Writer" /></li>
		<li>
			<ClickableButton url="/projects/to-do" label="To-do list" />
		</li>
		<li>
			<ClickableButton url="/projects/numbers" label="Info about a number" />
		</li>
		<li>
			<ClickableButton url="/projects/tvitr" label="Tvitr"></ClickableButton>
		</li>
		<li><ClickableButton url="/projects/exercises" label="Exercises" /></li>
	</div>
</ul>
