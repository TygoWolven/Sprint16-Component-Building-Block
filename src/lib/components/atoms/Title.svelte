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

<style>
  h1 {
    font-size: var(--fs-2xl) !important;
  }

  h2 {
    font-size: var(--fs-lg) !important;
  }

  h3 {
    font-size: var(--fs-md) !important;
  }

  .title-light {
    color: var(--accent2-primary);
  }
  .title-dark {
    color: var(--txt-dark-clr);
  }
</style>
