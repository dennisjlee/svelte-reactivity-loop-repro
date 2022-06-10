<script>

  import View from './_FakeView.svelte';

  let foo = {
    foo: 'foo',
    bar: 'bar'
  };

</script>

<View {foo} />
