<script>
  import Notes from "../lib/Notes.svelte";
  import logo from "../assets/logo.png";
</script>

<section>
  <div class="grid place-items-center">
    <h4>I am</h4>
    <h1>Scott Tolinski</h1>
    <img style="width: 300px;" src={logo} alt="Syntax Logo" />
    <br />
    <a href="https://twitter.com/stolinski">@stolinski</a>
    <a href="https://syntax.fm">Syntax.fm</a>
  </div>
  <Notes />
</section>

<style>
  h4 {
    color: var(--yellow) !important;
  }
</style>
