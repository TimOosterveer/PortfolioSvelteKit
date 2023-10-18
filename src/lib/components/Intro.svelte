<script>
	import { gsap } from 'gsap-trial';
	import { onMount } from 'svelte';

	/* The following plugin is a Club GSAP perk */
	import { SplitText } from 'gsap-trial/dist/SplitText';

	gsap.registerPlugin(SplitText);

	onMount(() => {
		let mySplitText = new SplitText('h1', { type: 'chars' });
		let chars = mySplitText.chars;

		gsap.from(chars, {
			yPercent: 90,
			stagger: 0.1,
			ease: "back.out",
			duration: 1
		});
	});
</script>

<section>
	<div class="info-me">
		<h1>TIM OOSTERVEER</h1>
		<p class="p">Student Frontend developer</p>
	</div>
</section>

<style>
	section {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100%;
		height: 90vh;
		padding: var(--padding);
	}
	
	h1 {
		overflow: hidden;
		color: var(--text-color-h1);
		font-size: 8rem;
		font-weight: 400;
		height: 22vh;
	}

	p {
		font-size: 24px;
		font-weight: 200;
		text-align: end;
		overflow: hidden;
	}
</style>
