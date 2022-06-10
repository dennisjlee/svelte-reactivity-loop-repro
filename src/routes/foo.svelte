<script>

  import View from './_FakeView.svelte';

  let foo = {
    foo: 'foo',
    bar: 'bar'
  };

</script>

<p>This page should load just fine when rendered via SPA.</p>
<p>Now try to refresh the page so it renders via SSR.</p>
<br>
<View {foo} />
