<script>
  import Demo from "./Demo.svelte";
  import Notes from "./Notes.svelte";

  export let title;
  export let parent;
  export let url;
  export let notes = "";
</script>

<section data-auto-animate data-background="#000">
  <h5 data-id="parent">{parent}</h5>
  <h1>{title}</h1>

  <Demo {title} {url} />
  <Notes>{notes}</Notes>
</section>
