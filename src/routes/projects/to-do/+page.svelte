<script lang="ts">
	type Task = {
		text: string;
		status: boolean;
	};
	let newTask: string = $state('');

	let tasks: Task[] = $state([]);
	function add() {
		tasks = [
			...tasks,
			{
				text: newTask,
				status: false
			}
		];
		newTask = '';
	}
</script>

<div class="justify-center flex">
	<div>
		<input type="text" bind:value={newTask} class="rounded-full text-black p-1" />
		<button onclick={add}>Dodaj</button>
	</div>
</div>
<div class="flex justify-center">
	<div class="w-6/12 rounded-2xl m-4 p-4 border-2 border-pink-600">
		<h1>Zadolžitve</h1>
		{#each tasks as task}
			<div>
				<p>
					<button onclick={() => (task.status = !task.status)}>{task.status ? '✅' : '❌'}</button>
					{task.text}
				</p>
			</div>
		{/each}
	</div>
</div>
