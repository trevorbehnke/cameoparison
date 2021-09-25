<script>
	import Welcome from "./screens/welcome.svelte"
	let state = "welcome"

	const start = e => {
		console.log(e );
	}
</script>

<main>
	{#if state === "welcome"}
		 <Welcome on:select={start}/>
	{:else if state === "playing"}
			<p>This is the game page.</p>
	{/if}
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>