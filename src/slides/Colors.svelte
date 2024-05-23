<script lang="ts">
  import Notes from "../lib/Notes.svelte";
  import chris from "../assets/chris.gif";
  import stairs from "../assets/stairs.gif";
  import ready from "../assets/ready.gif";
  import mrwave from "../assets/mrwave.gif";
  import Ship from "../lib/Ship.svelte";
</script>

<section>
  <section data-background="var(--yellow)">
    <h1 data-id="parent" style="color: #000 !important;">Color</h1>
  </section>
  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Color</h5>
    <h1>HDR Color via display-p3 & OKLCH</h1>
    <a target="_blank" href="https://oklch.com/#70,0.1,325,100"
      >OKLCH Color Picker</a
    >
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
.valid-css-oklch-colors {
  --color: oklch(92.06% 0.269 124.67)
  --opacity: oklch(92.06% 0.269 124.67 / .5);
  --white: oklch(100 none none);
  --black: oklch(none none none);
}
			`}
    </code></pre>

    <Notes
      >Lightness, Chroma, Hue. HDR, easy to type perceptually linear lightness.
      "Chroma is the colorfulness relative to the brightness of a similarly
      illuminated white,"</Notes
    >
  </section>

  <Ship
    versions={["111", "15.4", "113*"]}
    title="OKLCH"
    parent="Color"
    gif={stairs}
    ship_text="Ship it"
    caveat="Firefox doesn't support p3 yet"
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Color</h5>
    <h1>Color Mix</h1>
    <p>Mixes two colors together</p>

    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
				/* color: color-mix(in %color_space, %base_color %mix_percentage, %blend_color) */
				div {
					color: color-mix(in oklch, teal 50%, white)
				}
			`}
    </code></pre>
  </section>
  <Ship
    title="Color Mix"
    versions={["111", "16.2", "113"]}
    parent="Color"
    gif={mrwave}
    ship_text="Ship it"
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Color</h5>
    <h1>Color Contrast</h1>
    <p>Looks at first color, and return highest contrast color in list.</p>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
				div {
					background: var(--background);
					color: color-contrast(var(--background) vs tan, blue, #000);
				}
			`}
    </code></pre>
  </section>
  <Ship
    title="Color Contrast"
    parent="Color"
    gif={chris}
    ship_text="Check it"
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Color</h5>
    <h1>Relative Colors</h1>
    <p>
      <a
        target="_blank"
        href="https://preset-env.cssdb.org/blog/postcss-relative-color-syntax/"
        >https://preset-env.cssdb.org/blog/postcss-relative-color-syntax/</a
      >
    </p>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
.something {
  --color: red;
  /* transform red to hsl and manipulate its lightness */
  background: hsl(from var(--color) h s calc(l - 20%));
}
			`}
    </code></pre>
  </section>
  <Ship
    title="Relative Colors"
    parent="Color"
    gif={ready}
    ship_text="Ship it"
    versions={["", "16.4", ""]}
    caveat="With PostCSS"
  />
</section>
