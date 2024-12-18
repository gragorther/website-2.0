<script>
	import ClickableButton from "$lib/ClickableButton.svelte";
	import PageTitle from "$lib/PageTitle.svelte";

</script>

<PageTitle title="Exercises" />
<ul>
	<div class="flex flex-wrap gap-2 justify-center">
		<li><ClickableButton label="One" url="/projects/exercises/one" /></li>
		<li><ClickableButton label="Two" url="/projects/exercises/two" /></li>
		<li><ClickableButton label="Three" url="/projects/exercises/three" /></li>
	</div>
</ul>
