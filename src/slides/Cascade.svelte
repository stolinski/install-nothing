<script lang="ts">
  import Notes from "../lib/Notes.svelte";
  import murder from "../assets/murder.gif";
  import door from "../assets/door.gif";
  import goose from "../assets/goose.gif";
  import Ship from "../lib/Ship.svelte";

  const parent = "Cascade";
</script>

<section>
  <section data-background="var(--yellow)">
    <h1 data-id="parent" style="color: #000 !important;">{parent}</h1>
  </section>

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">{parent}</h5>
    <h1>:has</h1>
    <p>
      The parent selector. If parent, contains child, apply style to parent.
    </p>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
				.card:has(.cancel) {
					color: red;
				}
			`}
    </code></pre>
    <Notes>Behind flag in FF.</Notes>
  </section>

  <Ship
    title=":has"
    {parent}
    gif={murder}
    ship_text="Try it"
    versions={["105", "15.4", ""]}
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">{parent}</h5>
    <h1>Cascade Layers</h1>
    <p>You own private waterfalls</p>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
				@layer reset, base;

				@layer reset {
					body {
						padding: 0;
					}
				}

				@layer base {
					body {
						background: black;
					}
				}
			`}
    </code></pre>
    <Notes>All modern browser support TODAY.</Notes>
  </section>

  <Ship
    title="Cascade Layers"
    {parent}
    gif={goose}
    ship_text="Ship it"
    versions={["99", "15.4", "97"]}
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">{parent}</h5>
    <h1>@Property</h1>
    <p>Kinda like types for CSS variables.</p>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
@property --colorPrimary {
	syntax: '<color>';
	initial-value: magenta;
	inherits: false;
}

@layer base {
	body {
		background: black;
	}
}


`}
    </code></pre>
    <Notes
      >Basically Types for CSS. length number percentage length-percentage color
      image url integer angle time resolution transform-list transform-function
      custom-ident.</Notes
    >
  </section>

  <Ship
    title="@Property"
    {parent}
    gif={door}
    ship_text="Try it"
    versions={["85", "16.4", ""]}
  />
</section>
