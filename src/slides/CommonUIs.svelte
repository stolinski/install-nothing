<script lang="ts">
  import Notes from "../lib/Notes.svelte";
  import trash from "../assets/trash.webp";
</script>

<section>
  <section data-transition="fade">
    <h1>Have you ever built?</h1>
    <ul>
      <!-- BETA -->
      <li class="fragment fade-up">A modal?</li>
      <li class="fragment fade-up">A menu?</li>
      <li class="fragment fade-up">A mobile nav?</li>
      <li class="fragment fade-up">A drawer?</li>
      <li class="fragment fade-up">An accordion?</li>
      <!-- TODO -->
      <li class="fragment fade-up">Swiper?</li>
      <li class="fragment fade-up">Slideshow?</li>
      <!-- TODO Tooltips? -->
      <!-- MAYBE? -->
      <li class="fragment fade-up">Tabs?</li>
    </ul>
    <Notes>
      * Have you ever built any of these? They aren't the craziest UI items but
      they are things we need all the time. * When we do, we many times do one
      of two things
    </Notes>
  </section>

  <section>
    <h1>Reach for our handy JS Framework</h1>
    <Notes>
      * This is often the right answer, but in the same regard, instead of
      tossing everything into a div, we can utilize some new browser APIs do to
      much of the heavy lifting
    </Notes>
  </section>

  <section>
    <h1>`npm install ...`</h1>
    <img src={trash} alt="Trash" />
    <Notes>* Browsers are <mor></mor>e capable now than ever before</Notes>
  </section>
</section>

<style>
  h1 {
    --r-heading-color: var(--yellow);
    font-style: italic;
  }

  :global(.reveal) ul {
    list-style: none !important;
    text-align: center !important;
    margin: 0;
    padding: 0;
  }
  li {
    line-height: 1.8;
    margin: 0;
  }
</style>
