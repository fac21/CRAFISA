<script>
	export let name;
  import Box from './Box.svelte'
  let score = 0
</script>

<main style='background: url("tablecloth.jpg");'>
	<h1>Hello {name}!</h1>
  <Box bind:score={score} />
  <h2>Score: {score}</h2>
</main>

<style>
	main {
    height: 100vh;
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	}

	h1 {
		color: rgb(49, 119, 52);
    text-shadow: 5px 5px 5px white;
		text-transform: uppercase;
		font-size: 5em;
		font-weight: 700;
	}
  h2 {
    color: rgb(49, 119, 52);
    text-shadow: 5px 5px 5px white;
    position: absolute;
    width: 100%;
    bottom: 10%;  
    font-size: 3em;
    font-weight: 500;
  }
  
</style>