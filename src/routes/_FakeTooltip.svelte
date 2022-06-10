<script lang="ts">

  export let showTooltip = false;
</script>

{#if showTooltip}
  tooltip is showing
{:else}
  tooltip is not showing
{/if}