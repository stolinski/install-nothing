<script lang="ts">
  import Notes from "../lib/Notes.svelte";
</script>

<section data-transition="fade">
  <h1>What's up?</h1>
  <ul>
    <li class="fragment fade-up">
      We'll be looking at <i>real</i> demos using new and underutilized browser APIs
    </li>
    <li class="fragment fade-up">But can I actually use it?</li>
    <li class="fragment fade-up">
      🛳️ Ship score
      <ul>
        <li class="fragment fade-up">Check it</li>
        <li class="fragment fade-up">Try it</li>
        <li class="fragment fade-up">Ship it</li>
      </ul>
    </li>
  </ul>
  <Notes
    >* We're on the precipice of a massive amount of new browser APIs hit that
    great simplify our code.</Notes
  >
</section>

<style>
  h1 {
    color: var(--yellow) !important;
    font-style: italic;
  }
  li {
    line-height: 1.8;
    padding-left: 1rem;
  }
  li {
    list-style-type: "×";
  }
  li::marker {
    color: var(--teal);
  }
</style>
