<script lang="ts">
   let count = $state(0);
</script>

<div>
    <input type="number" bind:value={count}>
    <h1>{count}</h1>
</div>