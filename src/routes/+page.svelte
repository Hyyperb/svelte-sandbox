
<script>
	let version = "0.1";
	$: todolist = [
		"finish svelte tutorial",
		"like the video",
		"subscribe the channel"
	]

	function addTask(){
		let todo_item_input_box = document.getElementById("add");
		let task = todo_item_input_box.value;
		todolist = [...todolist, task];
		todo_item_input_box.value = null;
		todo_item_input_box.focus();
	}
	function cleanUp(){
		
	}
</script>

<!-- <style>
	p {
		font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
	}	
</style> -->

<h1> Todo list</h1>
<form>
	<input type="text" id="add" on:change={addTask}/> 
</form>
<button on:click={addTask}>Add</button>
<button on:click={cleanUp}>Clean up</button>
<div>
	{#each todolist as task ,i}

		<ul><input type="checkbox" id="task {i}"/>{task}</ul>
	{/each}
</div>