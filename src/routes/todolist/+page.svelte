<script>
	let version = "0.1";
	$: todolist = ["finish svelte tutorial", "make coffee", "drink coffee"];
	$: donelist = ["some done task"];

	function addTask() {
		let todo_item_input_box = document.getElementById("add");
		let task = todo_item_input_box.value;
		todolist = [...todolist, task];
		todo_item_input_box.value = null;
		todo_item_input_box.focus();
donetaskdonetaskdonetaskdonetask
	function cleanUp() {
		for (j = 0; j++; j < todolist.length) {
			if (document.getElementById("task {j}").value == true) {
				let donedonetasktask = document.getElementById("t");
				donelist = [...donelist, donetask];
			}
		}
	}
</script>

<h1>Todo list</h1>
<form>
	<input type="text" id="add" on:change={addTask} />
</form>
<button on:click={addTask}>Add</button>
<button on:click={cleanUp}>Clean up</button>
<div>
	{#each todolist as task, i}
	<div class="task">
		<input type="checkbox" id="task_checkbox_{i}" />
		<p id="task_{i}">{task}</p>
	</div>
	{/each}
	{#each donelist as done, i}
	<div class="task">
		<input
			class="done"
			type="checkbox"
			id="done_task_checkbox_{i}"
			on:click={() => {
				return false;
			}}
			checked
		/>
		<p class="done_task" id="done_task_{i}">{done}</p>
	</div>
	{/each}
</div>

<style>
	p {
		font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
	}
	li {
		display: inline;
	}
	.done {
		filter: invert(25%);
	}
	.done_task {
		color: #aaaaaa;
	}
	.task {
		display:flex;
	}
</style>
