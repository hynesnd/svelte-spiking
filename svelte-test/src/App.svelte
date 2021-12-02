
<!-- All the Javascript for our component goes inside script tags
at the top of the file. -->
<script> 
	
	import Button from './Button.svelte'
	import Heading from './Heading.svelte'

	/*State is managed in Svelte by declaring variables.
	when a variable is reassigned it triggers a DOM update
	This is v straightforward for primitives.
	For Arrays and Objects, we must make sure the function
	re-declares the variable to trigger the DOM update */
	
	let count = 0;
	let color = '#000000';

	const colors = ['#00ff00', '#ff0000', '#0000ff']

	let handleClick = () => {
		count++;
		color = colors[Math.floor(Math.random() * 3)];
	}
</script>

<main>
	<Heading count={count} />
	<Button color={color} handleClick={handleClick} />
</main>