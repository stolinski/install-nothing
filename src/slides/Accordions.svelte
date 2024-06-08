<script>
  import DemoSlide from "../lib/DemoSlide.svelte";
  import pocket from "../assets/pocket.gif";
  import Ship from "../lib/Ship.svelte";

  let parent = `Accordions`;
</script>

<section>
  <section>
    <h1 data-id="parent" style="color: var(--teal) !important;">
      {parent}
    </h1>
  </section>

  <DemoSlide title="Basic Accordion" url="demos/details/Details" {parent} />

  <DemoSlide title="Animating the Caret" url="demos/details/Caret" {parent} />

  <Ship
    title="<details> x <summary>"
    {parent}
    gif={pocket}
    versions={["12", "6", "49"]}
    global="97.5%!"
    ship_text="Ship It"
    notes="Been in Chrome since 2011, Safari 2012"
  />

  <DemoSlide
    title="WAAPI"
    url="demos/details/WAAPI"
    {parent}
    notes="Fully supported."
  />

  <DemoSlide
    title="View Transitions"
    url="demos/details/ViewTransitions"
    {parent}
    notes="Slide transitions are tougher this way without bringing in unsupported CSS APIs like @starting-style"
  />

  <DemoSlide
    title="CSS Only"
    url="demos/details/CSSOnly"
    {parent}
    notes="* this may or ay not work"
  />
</section>

<!-- TODO add ship to each demo slide as well -->
