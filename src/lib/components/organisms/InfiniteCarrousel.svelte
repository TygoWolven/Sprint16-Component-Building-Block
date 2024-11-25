<script>
    import LogoContainer from "../molecules/LogoContainer.svelte";
</script>

<div class="infinite-carrousel">
    <LogoContainer />
    <LogoContainer aria-hidden="true" />
</div>

<style>
    .infinite-carrousel {
        white-space: nowrap;
    }
    .infinite-carrousel:hover :global(.logo-container) {
        animation-play-state: paused;
    }
    .infinite-carrousel::before,
    .infinite-carrousel::after {
        position: absolute;
        z-index: 10;
        content: "";
        height: 50px;
        width: 250px;
        background: linear-gradient(
            to right,
            var(--accent2-primary),
            transparent
        );
        left: 0;
    }
    .infinite-carrousel::after {
        left: unset;
        right: 0;
        transform: rotateZ(180deg);
    }

    /* Media Query for small-screens */
    @media (max-width: 768px) {
        .infinite-carrousel::before,
        .infinite-carrousel::after {
            width: 50px;
        }
    }
</style>