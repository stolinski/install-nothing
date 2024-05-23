<script lang="ts">
  import Notes from "../lib/Notes.svelte";
  import pocket from "../assets/pocket.gif";
  import montel from "../assets/montel.gif";
  import lilou from "../assets/lilou.gif";
  import white from "../assets/white.gif";
  import Ship from "../lib/Ship.svelte";
</script>

<section>
  <section data-background="var(--yellow)">
    <h1 data-id="parent" style="color: #000 !important;">Media Queries</h1>
  </section>
  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Media Queries</h5>
    <h1>Media Range</h1>
    <h3 data-id="title">Was</h3>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
			@media (min-width: 400px) {
				/* Your lovely css */
			}
			`}
    </code></pre>
    <h3 data-id="title">Now</h3>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
    {@html `
			@media (400px <= width) {
				/* Your lovely css */
			}
    `}
    </code></pre>
    <Notes>I don't know about you, but I never remember this syntax.</Notes>
  </section>

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Media Queries</h5>
    <h1>Media Range</h1>

    <h3 data-id="title">{"> < >= <="}</h3>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
    {@html `
			@media (400px <= width <= 1000px) {
				/* Your lovely css */
			}
    `}
    </code></pre>
  </section>

  <Ship
    title="Media Range"
    parent="Media Queries"
    gif={pocket}
    versions={["104", "16.4", "63"]}
    ship_text="Ship It"
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Media Queries</h5>
    <h1>Custom Media Queries</h1>

    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
    {@html `
			@custom-media --above_med (width > 700px);

			@media (--above_med) {
				grid-template-columns: repeat(var(--med-cols), 1fr);
			}
    `}
    </code></pre>
  </section>

  <Ship
    title="Custom Media Queries"
    parent="Media Queries"
    gif={montel}
    ship_text="Ship It"
    caveat="with PostCSS"
    hide_logos={true}
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Media Queries</h5>
    <h1>Container Queries</h1>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
    {@html `
			.card-container {
				container-type: inline-size;
				container-name: card;
				/* or just */
				container: card / inline-size;
			}


			@container card (width > 300px) {
				.card {
					font-size: 2em;
				}
			}
    `}
    </code></pre>
  </section>

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Media Queries</h5>
    <h1>Container Query Units</h1>

    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
    {@html `
			cqw: 1% of a query container's width
			cqh: 1% of a query container's height
			cqi: 1% of a query container's inline size
			cqb: 1% of a query container's block size
			cqmin: The smaller value of either cqi or cqb
			cqmax: The larger value of either cqi or cqb
    `}
    </code></pre>
  </section>

  <Ship
    title="Container Queries & Units"
    parent="Media Queries"
    gif={lilou}
    ship_text="Ship It"
    versions={["106", "16.0", "110"]}
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">Media Queries</h5>
    <h1>Container Style Query</h1>

    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
    {@html `
			.card-container {
				container-type: inline-size;
				--theme: wave-race;
			}

			@container style(--theme: wave-race) {
				.card {
					background: teal;
				}
			}
    `}
    </code></pre>
    <Notes
      >Behind a flag in chrome canary. "Can't we fix by adding a class name?"
      Yes, but more targeted. Components at a theme level. Style queries with a
      custom property in chrome 111</Notes
    >
  </section>

  <Ship
    title="Style Queries"
    parent="Media Queries"
    gif={white}
    ship_text="Check it"
  />
</section>
