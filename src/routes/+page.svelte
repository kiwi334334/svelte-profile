<script lang="ts">
	let count = $state(0);
	let customMessage = $state('');
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
		'In Response: Counter Spell',
        'Your Father Smelt Of Elder Berrys',
        'Advance Speed To Ludicrous Speed!'
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
		<input bind:value={customMessage} placeholder="Add Custom Messages Here">
		<button on:click={() => {arrayWithAllMessages.push(customMessage); customMessage = ''}}>Submit Your Custom Message</button>
	<br>
	<button
		on:click={() => {
			count += 1;
			if (count > arrayWithAllMessages.length) {
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
        padding:0;
        margin: 0;
	}
	span {
		color: blueviolet;
	}
</style>
