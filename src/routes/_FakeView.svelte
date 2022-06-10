<script lang="ts">
  import FakeTooltip from './_FakeTooltip.svelte';

  export let foo;

  $: viewModels = createViewModels(foo);

  function createViewModels(foo) {
    console.log('in createViewModels');
    return [
      {
        label: 'foo',
        value: foo.foo
      },
      {
        label: 'bar',
        value: foo.bar
      }
    ];
  }
</script>

View models:
{#each viewModels as viewModel}
  <div>
    {viewModel.label}: {viewModel.value}
    <FakeTooltip bind:showTooltip={viewModel.showTooltip} />
  </div>
{/each}
