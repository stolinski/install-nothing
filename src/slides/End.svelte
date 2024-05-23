<script>
  import qr from "../assets/show.png";

  export let no_thanks = false;
</script>

<section>
  <img src={qr} alt="https://tolin.ski/talks/fresh-style" width="200" />
  <p>
    <a href="https://tolin.ski/talks/fresh-style"
      >https://tolin.ski/talks/fresh-style</a
    >
  </p>
  {#if !no_thanks}
    <h1>Thank you</h1>
  {/if}
</section>
