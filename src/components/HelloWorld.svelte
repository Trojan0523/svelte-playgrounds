<script lang="ts">
    export const name = "svelte";

    let count = 1;

    function increment() {
        count += 1;
    }
</script>

<h1>Hello {name}</h1>

<button on:click={increment}>Click me ~ {count}</button>

{#if count > 10}
    <div>{count} is less than 10</div>
{:else if count > 12}
    <div>{count} is between 10 and 12</div>
{:else}
    <div>{count} is greater than 12</div>
{/if}
