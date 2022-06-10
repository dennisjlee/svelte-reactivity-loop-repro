<script>
  export let expanded = false;
</script>

<p>
  <button on:click={() => expanded = !expanded}>
    {#if expanded}
      Collapse
    {:else}
      Expand
    {/if}
  </button>
</p>

{#if expanded}
  <slot />
{/if}
