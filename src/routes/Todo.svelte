<script>
	let todoItem = '';

	let todoItems = [{ text: '', status: '' }];

	function addTodo() {
		todoItems = [...todoItems, { text: todoItem, status: false }];
		localStorage.setItem('todo', JSON.stringify(todoItems));
		newItem: '';
	}

	function removeTodo(index) {
		todoItems.splice(index, 1);
		todoItems = todoItems;
	}
</script>

<div>
	<input bind:value={todoItem} name="todo" type="text" placeholder="add todo" />
	<button on:click={addTodo}>add</button>

	<div>
		{#each todoItems as item, index}
			<input type="checkbox" bind:checked={item.status} />
			<span class:checked={item.status}>{item.text}</span>
			<span on:click={() => removeTodo(index)}>❌</span>
		{/each}
	</div>
</div>

<style>
</style>
