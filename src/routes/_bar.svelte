<script>
  import Expander from './_expander.svelte';

  export let selectedId;
  export let models;

  $: expandedById = {
    [selectedId ?? models.submodels[0]?.id]: true
  };

</script>

{#each models.submodels as submodel, index (submodel.id)}
  <div>
    id: {submodel.id}<br>
    <Expander bind:expanded={expandedById[submodel.id]}>
      Details: {submodel.details}
    </Expander>
  </div>
{/each}
