<script>
    import InfiniteCarrousel from '$lib/components/organisms/InfiniteCarrousel.svelte'
    import Title from '$lib/components/atoms/Title.svelte'
</script>

<!-- In de leertaak is het component volledig geïntegreerd met dynamische data en een betere structuur -->
<section>
    <Title 
      headertype='h2'
      content='Partners' 
      color='dark' />
    <InfiniteCarrousel />
</section>

<style>
  section {
    text-align: center;
    text-transform: uppercase;
  }
</style>