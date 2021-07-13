<script>
	export let name;
  import Box from './Box.svelte'
  let score = 0
</script>

<main>
	<h1>Hello {name}!</h1>
  <Box bind:score={score} />
  <h2>Score: {score}</h2>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 400;
	}
  h2 {
    position: absolute;
    width: 100%;
    bottom: 10%;
  }
</style>