<script lang="ts">
  import Notes from "../lib/Notes.svelte";
  import ll from "../assets/ll.gif";
  import robo from "../assets/robocop.gif";
  import hat from "../assets/hat.gif";
  import vin from "../assets/vin.gif";
  import Ship from "../lib/Ship.svelte";

  const parent = "Animation";
  const card_1 = "View Transitions";
  const card_2 = "Scroll Animations";
  const card_3 = "Animation Composition";
  const card_4 = "linear()";
</script>

<section>
  <section data-background="var(--yellow)">
    <h1 data-id="parent" style="color: #000 !important;">{parent}</h1>
  </section>

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">{parent}</h5>
    <h1>{card_1}</h1>
    <p>Native app style transitions on the web.</p>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
::view-transition-old(root),
::view-transition-new(root) {
  animation-duration: 1s;
}

@keyframes slide {
  from { transform: translateX(30px); }
}

::view-transition-old(root) {
  animation: 300ms cubic-bezier(0.4, 0, 0.2, 1) both slide;
}

::view-transition-new(root) {
  animation: 300ms cubic-bezier(0.4, 0, 0.2, 1) both slide;
}
			`}
    </code></pre>
  </section>

  <Ship
    title={card_1}
    {parent}
    gif={vin}
    ship_text="Try it"
    versions={["111", "", ""]}
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">{parent}</h5>

    <h1>{card_2}</h1>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
				@keyframes fade { … }

				.item {
					animation: fade linear;
					animation-timeline: scroll(root block);
					/* nearest, root, self */
					/* block, inline, y, x */
				}
			`}
    </code></pre>
  </section>

  <Ship
    title={card_2}
    {parent}
    gif={hat}
    ship_text="Check it"
    notes="Try behind a flag if you dare"
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">{parent}</h5>
    <h1>{card_3}</h1>
    <p>Add multiple animations without interrupting.</p>
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
			div {
				animation-composition: add;
			}
			`}
    </code></pre>
  </section>

  <Ship
    title={card_3}
    {parent}
    gif={ll}
    ship_text="Try it"
    notes="Behind a flag in FF."
    versions={["112", "16.0", ""]}
  />

  <section data-auto-animate data-background="#000">
    <h5 data-id="parent">{parent}</h5>
    <h1>{card_4}</h1>
    <p />
    <pre data-id="code"><code data-line-numbers class="hljs" data-trim>
			{@html `
div {
	animation-timing-function: linear(0, 0.218 2.1%, 0.862 6.5%, 1.114, 1.296 10.7%, 1.346, 1.37 12.9%, 1.373, 1.364 14.5%, 1.315 16.2%, 1.032 21.8%, 0.941 24%, 0.891 25.9%, 0.877, 0.869 27.8%, 0.87, 0.882 30.7%, 0.907 32.4%, 0.981 36.4%, 1.012 38.3%, 1.036,1.046 42.7% 44.1%, 1.042 45.7%, 0.996 53.3%, 0.988, 0.984 57.5%, 0.985 60.7%,1.001 68.1%, 1.006 72.2%, 0.998 86.7%, 1);
}
			`}
    </code></pre>
    <Notes>No Safari, but it's in FF. 40% Support</Notes>
  </section>

  <Ship
    title={card_4}
    {parent}
    gif={robo}
    ship_text="Try it"
    notes="In Chrome and FF"
    versions={["113", "", "112"]}
  />
</section>
