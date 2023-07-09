<script>
	// @ts-nocheck
/* ------------------------------- Components ------------------------------- */
	import { onMount } from 'svelte';
    import About from './about.svelte';

/* --------------------------------- plugins -------------------------------- */
	import Reveal from 'reveal.js';
	import Markdown from 'reveal.js/plugin/markdown/markdown';
	import Highlight from 'reveal.js/plugin/highlight/highlight';
	import Notes from 'reveal.js/plugin/notes/notes';
	import Animate from 'reveal.js/plugin/animate/animate.esm.js';
	import Simplemenu from 'reveal.js/plugin/simplemenu/plugin/simplemenu/simplemenu';
	// import 'reveal.js/plugin/simplemenu/plugin/simplemenu/simplemenu.css';
	import Verticator from 'reveal.js/plugin/verticator/plugin/verticator/verticator';

/* ------------------------------- stylesheets ------------------------------ */
    import 'animate.css';
    import 'reveal.js/dist/reveal.css';
    import 'reveal.js/dist/theme/black.css';
    import 'reveal.js/plugin/highlight/monokai.css';
    import 'reveal.js/plugin/verticator/plugin/verticator/verticator.css';

/* -------------------------------- functions ------------------------------- */

/* ---------------------------- Liyfecycle Events --------------------------- */
	onMount(() => {
		// @ts-ignore
		const deck = new Reveal({
			autoAnimateEasing: 'ease',
			autoAnimateDuration: 1,
			hash: true,
			controls: true,
			progress: false
		});

		deck.initialize({
			plugins: [Markdown, Highlight, Notes, Animate, Verticator, Simplemenu],
			animated: {
				H1: { animated: 'slideInDown' },
				IMG: { animated: 'backInDown', repeat: 'repeat-2', speed: 'slower' },
				P: { animated: 'bounceInRight', speed: 'fast' },
				UL: { animated: 'jello', repeat: 'infinite', speed: 'slower' }
			},
			verticator: {
				csspath: 'reveal.js/plugin/verticator/plugin/verticator/verticator.css'
			},
			simplemenu: {
				csspath: false
			}
		});
	});
</script>

<div class="reveal">
	<div class="slides">
		<section id="home">slide 1</section>
		<section id="khedma">
			<!-- <h1>Hello</h1>
			<p>There</p> -->
			<section>slide 3.1</section>
			<section>slide 3.1</section>
			<section>slide 3.1</section>

		</section>
        <About />
		<!-- <section id="about">
			<section>slide 3.1</section>
			<section>
				slide 3.2 <ul>
					Hey there <li>hello</li>
					<li>hi</li>
				</ul>
			</section>
		</section> -->
		<section id="contact">slide 4</section>
	</div>
</div>
