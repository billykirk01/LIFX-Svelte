<script>
    export let lights;
</script>

{#await lights then lights}
    {#each lights as light}
        <p>{light.label} - {light.power}</p>
    {/each}
{/await}
