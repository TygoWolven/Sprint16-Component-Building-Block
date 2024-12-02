<script>
  import LogoContainer from "../molecules/LogoContainer.svelte";
</script>

<!-- Added aria-labels so screenreaders won't read the list twice -->
<div class="infinite-carrousel">
  <LogoContainer hidden="false" />
  <LogoContainer hidden="true" />
</div>

<style>
  .infinite-carrousel {
    white-space: nowrap;
    margin: var(--margin) 0;
  }
  .infinite-carrousel:hover :global(.logo-container) {
    animation-play-state: paused;
  }

  /* Fade-away on sides of the carrousel */
  .infinite-carrousel::before,
  .infinite-carrousel::after {
    position: absolute;
    content: "";
    left: 0;
    width: 15%;
    z-index: 10;
    height: clamp(3rem, 5vw, 7rem);
    background: linear-gradient(
      to right,
      white,
      transparent
    );
  }
  .infinite-carrousel::after {
    transform: rotateZ(180deg);
    left: unset;
    right: 0;
  }
</style>