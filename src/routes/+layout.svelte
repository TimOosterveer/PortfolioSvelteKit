<script>
	import { onMount } from 'svelte';
  import Lenis from "@studio-freight/lenis";

	onMount(() => {
		const lenis = new Lenis();

		lenis.on('scroll', (e) => {
			console.log(e);
		});

		function raf(time) {
			lenis.raf(time);
			requestAnimationFrame(raf);
		}

		requestAnimationFrame(raf);

	});
</script>

<slot />
