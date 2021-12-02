<script>
  // The export variable syntax below is how svelte components receive props.
  export let count;
</script>

<h1>Hello, I am a svelte app!</h1>
<h2>The following button has been clicked {count} times.</h2>