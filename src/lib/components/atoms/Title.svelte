<script>
  export let headertype = ''
  export let content = ''
  export let color = ''
</script>

{#if headertype === 'h1' }
  <h1 class="title-{color}">
    {content}
  </h1>
{:else if headertype === 'h2' }
  <h2 class="title-{color}">
    {content}
  </h2>
{:else if headertype === 'h3' }
  <h3 class="title-{color}">
    {content}
  </h3>
{/if}

<!-- In de leertaak maak ik gebruik van variabele waardes, die ik hier niet kan gebruiken -->
<style>
  h1, h2, h3 {
    margin-bottom: 1rem;
  }
  h1 {
    font-size: 3.5rem;
  }
  h2 {
    font-size: 2.5rem;
  }
  h3 {
    font-size: 1.5rem;
  }

  .title-light {
    color: white;
  }
  .title-dark {
    color: black;
  }
</style>
