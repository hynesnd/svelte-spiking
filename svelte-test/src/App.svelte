
<!-- All the Javascript for our component goes inside script tags
at the top of the file. -->
<script> 
	
	import ArrButton from './ArrButton.svelte';
import Button from './Button.svelte'
	import Heading from './Heading.svelte'

	/*State is managed in Svelte by declaring variables.
	when a variable is reassigned it triggers a DOM update
	This is v straightforward for primitives.
	For Arrays and Objects, we must make sure the function
	re-declares the variable to trigger the DOM update */
	
	let count = 0;
	let color = '#000000';
	let testArr = [1, 2, 3]

	const colors = ['#00ff00', '#ff0000', '#0000ff']

	const handleClick = () => {
		count++;
		color = colors[Math.floor(Math.random() * 3)];
	}

	const pushArr = () => {
		testArr = [...testArr, testArr.length + 1];
	}

	const popArr = () => {
		testArr = [...testArr.slice(0, -1)];
	}
</script>

<main>
	<Heading count={count} testArr={testArr}/>
	<Button color={color} handleClick={handleClick} />
	<ArrButton pushArr={pushArr} popArr={popArr} />
</main>