<script>
  // The export variable syntax below is how svelte components receive props.
  export let count;
  export let testArr
</script>

<h1>Hello, I am a svelte app!</h1>
<h2>The following button has been clicked {count} times.</h2>
<h2>The test array looks like this: {testArr}</h2>