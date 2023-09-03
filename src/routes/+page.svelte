<script>
	import Todo from './Todo.svelte';
</script>

<svelte:head>
	<title>Todo App</title>
	<meta name="description" content="Todo App" />
</svelte:head>

<section>
	<h1>
		<span class="welcome"> Todo App </span>
	</h1>
	<Todo />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}
</style>
