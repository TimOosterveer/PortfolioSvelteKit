<script>
	import { gsap } from 'gsap';
	import { onMount } from 'svelte';

	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	import { backIn, backOut } from 'svelte/easing';
	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		gsap.from('.about-me', {
			scrollTrigger: {
				trigger: '.info-me',
				start: '-100px',
				end: '400px',
				scrub: 'true',
			},
			y: 200,
		});

		gsap.from('.intro', {
			scrollTrigger: {
				trigger: '.info-me',
				start: '-100px',
				end: '400px',
				scrub: 'true',
			},
			y: 300,
		});

	});
</script>

<section class="section-about">
	<p class="about-me">
		"Ik ben Tim Oosterver, een gepassioneerde student frontend developer die gedreven is om
		verbluffende digitale projecten te creëren. Mijn focus ligt op het omzetten van concepten in
		esthetisch aantrekkelijke en functionele websites en applicaties. Mijn werk weerspiegelt mijn
		toewijding aan innovatie en mijn liefde voor het vak."
	</p>

	<div class="intro">
		<img src="timmiepf.jpeg" alt="" />
	</div>
</section>

<style>
	section {
		position: sticky;
		top: 3rem;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: #1a535c;
		color: var(--text-color-light);
		border-radius: 10px;
		height: 90vh;
		padding: var(--padding);
		overflow: hidden;
	}

	p {
		font-size: 24px;
		font-weight: 200;
		width: 45vw;
		overflow-y: hidden;
	}

	.intro {
		height: 100%;
		width: 30%;
	}

	img {
		width: 100%;
		height: 100%;
		border-radius: 10px;
		object-fit: cover;
	}

	@media screen and (max-width: 767px) {

		section {
			display: flex;
			flex-direction: column;
			height: 100%;
		}

		p {
			width: 100%;
		}

		.intro {
			width: 100%;
			height: 100%;
		}

		img {
			display: none;
		}

	}
</style>
