<script>
	import ClickableButton from '$lib/ClickableButton.svelte';
	import PageTitle from '$lib/PageTitle.svelte';
</script>

<PageTitle title="Projects" />
<p class="text-center">Stuff I made at a coding class</p>
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li><ClickableButton href="/projects/writer">Writer</ClickableButton></li>
		<li>
			<ClickableButton href="/projects/to-do">To-Do list</ClickableButton>
		</li>
		<li>
			<ClickableButton href="/projects/numbers">Numbers</ClickableButton>
		</li>
		<li>
			<ClickableButton href="/projects/tvitr">Tvitr</ClickableButton>
		</li>
		<li><ClickableButton href="/projects/exercises">Exercises</ClickableButton></li>
	</div>
</ul>
