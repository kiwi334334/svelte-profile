<script lang="ts">
   let count = $state(0);
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
    <button onclick={() => {count += 1; if(count > 9) {count = 0 }}}>{arrayWithAllMessages[count]}</button>
</div>

<style>
    :root {
        background: skyblue;
    }
</style>