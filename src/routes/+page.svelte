<script lang="ts">
	let count = $state(0);
	let leftLimit = $state(0);
	let righLimit = $state(1);
	let arrayWithAllMessages = $state([
		'Hello World',
		'Why Would You Do This',
		'How Dare You!',
		'Who are you?',
		'AlphaSONIC!!!',
		'Luke I Am Your Father',
		'Hello There',
		'Subway Eat Fresh',
		'NOOOOOOOOOOOOOOOOOOOOOOOOOOOO!',
		'In Response: Counter Spell'
	]);
</script>

<div>
	<button
		on:click={() => {
			leftLimit += 1;
		}}>Increase Left Character Limit</button
	>
	<button
		on:click={() => {
			leftLimit -= 1;
		}}>Decrease Left Character Limit</button
	>
	<br />
	<button
		on:click={() => {
			righLimit += 1;
		}}>Increase Right Character Limit</button
	>
	<button
		on:click={() => {
			righLimit -= 1;
		}}>Decrease Right Character Limit</button
	>
    <br>
	<button
		on:click={() => {
			count += 1;
			if (count > 9) {
				count = 0;
			}
		}}>Cycle Messages</button
	>
	<h1>
		the characters in the string between {leftLimit}-{righLimit} are
		<span>{arrayWithAllMessages[count].substring(leftLimit, righLimit)}</span>
	</h1>
</div>

<style>
	:root {
		background: skyblue;
	}
	span {
		color: blueviolet;
	}
</style>
