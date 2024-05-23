<script lang="ts">
  import Notes from "../lib/Notes.svelte";
</script>

<section data-transition="fade">
  <h1>What are we doing here?</h1>
  <ul>
    <li class="fragment fade-up">
      <i>Wow</i> techniques with new and coming CSS features
    </li>
    <li class="fragment fade-up">
      Give it a ship score
      <ul>
        <li class="fragment fade-up">Check it</li>
        <li class="fragment fade-up">Try it</li>
        <li class="fragment fade-up">Ship it</li>
      </ul>
    </li>
  </ul>
  <Notes>
    * My job lets me see new things * Newer than chatGPT * People always say...
    that's cool but I can't use it
  </Notes>
</section>

<style>
  h1 {
    color: var(--yellow) !important;
  }
  li {
    line-height: 1.8;
  }
</style>
