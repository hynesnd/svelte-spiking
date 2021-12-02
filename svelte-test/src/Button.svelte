<script>
  export let handleClick
  export let color
</script>

<!-- Different event listener syntax for onClick! -->
<button style="--color: {color}" on:click={handleClick}>
Click me!
</button>

<!-- Can add in-line styling which is scoped just to this component 
There's a bit of extra work required to get styling to work from a variable as with background colour-->
<style>
  button {
    color: white;
    background-color: var(--color);
  }
</style>