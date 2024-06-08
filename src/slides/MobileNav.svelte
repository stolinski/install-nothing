<script>
  import DemoSlide from "../lib/DemoSlide.svelte";
  let parent = `Mobile Nav × Drawer`;
</script>

<section>
  <section>
    <h1 data-id="parent" style="color: var(--teal) !important;">
      {parent}
    </h1>
  </section>

  <DemoSlide title="WAAPI" url="demos/mobile-nav/WAAPI" {parent} />

  <DemoSlide
    title="View Transitions"
    url="demos/mobile-nav/ViewTransitions"
    {parent}
  />

  <DemoSlide
    title="CSS Only Mobile Nav"
    url="demos/mobile-nav/CSSOnly"
    {parent}
    notes="Responds to keyboard events and also supports click-to-close."
  />

  <DemoSlide title="Drawrer w/ CSS" url="demos/details/CSS" {parent} />
</section>
