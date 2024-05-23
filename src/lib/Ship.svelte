<script lang="ts">
  import Logos from "./Logos.svelte";
  import Notes from "./Notes.svelte";

  export let title;
  export let parent;
  export let gif;
  export let ship_text;
  export let caveat = "";
  export let notes = "";
  export let versions = ["", "", ""];
  export let hide_logos = false;
</script>

<section data-auto-animate data-background="#000">
  <h5>{parent}</h5>
  <h1>{title}</h1>

  <h3 data-id="title">Ship Score</h3>
  <div class="fragment zoom">
    <h2
      class="ship"
      class:know={ship_text === "Check it"}
      class:try={ship_text === "Try it"}
    >
      {ship_text}<br />
      {#if caveat}
        <span class="caveat">* {caveat}</span>
      {/if}
    </h2>
    {#if !hide_logos}
      <Logos ff_v={versions[2]} saf_v={versions[1]} c_v={versions[0]} />
    {/if}
    <img src={gif} alt="" />
  </div>
  <Notes>{notes}</Notes>
</section>

<style>
  .caveat {
    font-size: 0.3em;
    position: absolute;
    right: -70px;
    background: var(--yellow);
    padding: 10px;
    top: 57px;
    z-index: -1;
  }

  .ship {
    font-size: 4.2rem;
    background: var(--yellow);
    color: black !important;
    position: absolute;
    font-style: italic;
    rotate: -5deg;
    inset: auto;
    padding: 0 20px;
    left: 50%;
    translate: -50% -90px;
    box-shadow: 0 0 10px 10px oklch(0% 0 100 / 0.3);
    z-index: 10;
  }
  .ship.know {
    background: var(--red);
  }
  .ship.try {
    background: var(--teal);
  }
</style>
