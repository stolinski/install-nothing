<script>
  import qr from "../assets/show.png";

  export let no_thanks = false;
</script>

<section>
  <!-- TODO replace this QR Code -->
  <img src={qr} alt="https://tolin.ski/talks/install-nothing" width="200" />
  <p>
    <a href="https://tolin.ski/talks/install-nothing"
      >https://tolin.ski/talks/install-nothing</a
    >
  </p>
  {#if !no_thanks}
    <h1>Thank you</h1>
  {/if}
</section>
