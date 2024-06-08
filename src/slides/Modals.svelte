<script>
  import DemoSlide from "../lib/DemoSlide.svelte";
  import Ship from "../lib/Ship.svelte";

  import Demo from "../lib/Demo.svelte";
  import Notes from "../lib/Notes.svelte";
  import pocket from "../assets/pocket.gif";
  import grid from "../assets/gridCIU.png";
  import white from "../assets/white.gif";

  let parent = `Modals × Alerts × Dialogs`;
</script>

<section>
  <section>
    <h1 data-id="parent" style="color: var(--teal) !important;">
      {parent}
    </h1>
  </section>

  <DemoSlide title="Basic Modal" url="demos/dialog/Modal" {parent} />

  <Ship
    title="Dialog Element"
    {parent}
    gif={pocket}
    versions={["37", "15.4", "98"]}
    global="96%!"
    ship_text="Ship It"
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">A note on availability</h5>
    <img src={grid} alt="CSS Grid Can I Use." />
    <Notes
      >If you think 96% isn't enough just know that flexbox support is also at
      96%!</Notes
    >
  </section>

  <DemoSlide title="Animating With WAAPI" url="demos/dialog/WAAPI" {parent} />

  <Ship
    title="Web Animations API"
    {parent}
    gif={white}
    versions={["84", "13.1", "75"]}
    ship_text="Ship it"
    global="97%"
  />

  <DemoSlide
    title="View Transitions"
    url="demos/dialog/ViewTransitions"
    {parent}
  />

  <Ship
    title="View Transitions API"
    {parent}
    gif={white}
    versions={["111", "TP", ""]}
    global="72%"
    ship_text="Try it"
  />

  <DemoSlide title="Animating With CSS" url="demos/dialog/CSS" {parent} />

  <Ship
    title="@starting-style"
    {parent}
    gif={white}
    versions={["117", "17.6", ""]}
    ship_text="Try it"
    global="72%"
  />

  <Ship
    title="allow-discrete"
    {parent}
    gif={white}
    versions={["117", "", ""]}
    global="71%"
    ship_text="Try it"
  />
</section>
