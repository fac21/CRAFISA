<script>
  export let score

  let interval;
  let isIntervalRunning = false

  let topPosition = 40
  let leftPosition = 40

  function moveCube() {
  topPosition = Math.min(Math.random()*100, 90)
  leftPosition = Math.min(Math.random()*100, 90)
  }

  function mouseLeave() {
    if (isIntervalRunning) {
    alert('YOU GOT CAUGHT BY ANTONIO')
    clearInterval(interval)
    isIntervalRunning = false
    topPosition = 40
    leftPosition = 40
    }
  }

  function myInterval() {
    if (!isIntervalRunning) {
    score = 0
    interval = setInterval(() => {score++; moveCube()}, 1000)
    isIntervalRunning = true
    }
  }

</script>

<!-- {#if !isIntervalRunning} -->
<img class='box' 
on:mouseleave={mouseLeave} 
on:click={myInterval} 
style='top: {topPosition}vh; left: {leftPosition}vw; cursor: url("smallpineapple.png"), auto;' 
src="pizza.png" 
alt="Antonio's nightmare"/>
  <!-- <p>{topPosition}</p> -->
<!-- {/if} -->

<style>
  img {
    position: absolute;
    height: 200px;
    width: 200px;
    top: 40vh;
    left: 40vw;
    transition: top linear 2s, left linear 2s; 
    border-radius: 100%;
  }
</style>