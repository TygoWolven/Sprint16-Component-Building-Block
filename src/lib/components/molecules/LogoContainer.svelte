<script>
    import { Vibe, Lillet, Pernod, Bacardi, Hendricks, Leonista, London, Absolut, Cola, Passoa } from '$lib/assets/partners.js' 
</script>

<div class="logo-container">
    <img src={Vibe} alt="Vibe">
    <img src={Lillet} alt="Lillet">
    <img src={Pernod} alt="Pernod Ricard">
    <img src={Bacardi} alt="Bacardi">
    <img src={Hendricks} alt="Hendricks Gin">
    <img src={Leonista} alt="Leonista">
    <img src={London} alt="The London Essence">
    <img src={Absolut} alt="Absolut Vodka">
    <img src={Cola} alt="Coca Cola">
    <img src={Passoa} alt="Passoa">
</div>

<style>
    .logo-container {
        display: inline-block;
        animation: 35s slide infinite linear;
    }
    .logo-container img {
        height: 3vw;
        min-height: 30px;
        margin: 0 40px;
    }
     @keyframes slide {
        from {
          transform: translateX(0);
        }
        to {
          transform: translateX(-100%);
        }
    }

    @media (prefers-reduced-motion) {
    .logo-container {
        animation: none;
    }
  }
</style>