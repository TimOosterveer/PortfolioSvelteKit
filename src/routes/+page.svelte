<script>
	import Intro from '../lib/components/Intro.svelte';
	import IntroTekst from '../lib/components/IntroTekst.svelte';
	import LastProjects from '../lib/components/LastProjects.svelte';
	import AllProjects from '../lib/components/AllProjects.svelte';
</script>

<Intro />
<IntroTekst />
<LastProjects />
<AllProjects />

<style>
	:global(*) {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}

	:global(:root) {
		--background-color: #242424;
		--background-color-light: #2d6ed09a;
		--text-color-h1: #f5b19c;
		--text-color-dark: #1a202c;
		--text-color-light: #f0eff4;

		--padding: 2rem;
	}
</style>
