<script>
  import DemoSlide from "../lib/DemoSlide.svelte";
  import Ship from "../lib/Ship.svelte";
  import pocket from "../assets/pocket.gif";

  let parent = `Menus × Popovers`;
</script>

<section>
  <section>
    <h1 data-id="parent" style="color: var(--teal) !important;">
      {parent}
    </h1>
  </section>

  <DemoSlide title="Basic Popover" url="demos/popover/Basic" {parent} />

  <DemoSlide title="All Action, no JS" url="demos/popover/Action" {parent} />

  <!-- TODO GIF -->
  <Ship
    title="Popover"
    {parent}
    gif={pocket}
    versions={["114", "17", "125"]}
    global="96%!"
    ship_text="Ship It"
    notes="this thing rules. the only bummer is anchor positioning"
  />

  <DemoSlide
    title="WAAPI × JS Anchor"
    url="demos/popover/Compat"
    {parent}
    notes="
		* intersting thing about popover is that it pust on the top-layer, that creates a new stacking context, position relative won't work
		*listening for scroll is not ideal but, who really scrolls when the nav is open.  *what does it take to have an anchored popover with animations using only APIs you can use today."
  />

  <DemoSlide
    title="CSS Only w/Anchor"
    url="demos/popover/Anchor"
    {parent}
    notes="* this may or ay not work"
  />

  <Ship
    title="Anchor"
    {parent}
    gif={pocket}
    versions={["125", "", ""]}
    global="48%!"
    ship_text="Check It"
    notes="The API is still in discussion with conversation still solidifying the direction."
  />
</section>
