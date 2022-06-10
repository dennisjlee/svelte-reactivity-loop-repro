<script>

  import Bar from './_Bar.svelte';

  let selectedId = null;
  let models = {
    submodels: [
      {
        id: '123',
        details: 'Lorem ipsum'
      },
      {
        id: '234',
        details: 'dolor sit amet'
      }
    ]
  };

</script>

this is route /foo

<Bar {selectedId} {models}/>
