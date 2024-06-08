<script>
  import DemoSlide from "../lib/DemoSlide.svelte";
  let parent = `Drawer`;
</script>

<section>
  <section>
    <h1 data-id="parent" style="color: var(--teal) !important;">
      {parent}
    </h1>
  </section>

  <DemoSlide title="Basic Drawer" url="demos/details/HTML" {parent} />
  <DemoSlide title="Drawer w/ WAAPI" url="demos/details/DialogJS" {parent} />
  <DemoSlide title="Drawrer w/ CSS" url="demos/details/CSS" {parent} />
</section>
