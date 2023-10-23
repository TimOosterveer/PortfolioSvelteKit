<script>
	import { gsap } from 'gsap-trial';
	import { onMount } from 'svelte';

	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		gsap.from('.last-projects', {
			scrollTrigger: {
				trigger: '.section-about',
				start: 'top',
				end: 'bottom',
				scrub: 'true'
			},
			y: 300
		});

		gsap.from('.second-project', {
			scrollTrigger: {
				trigger: '.section-about',
				start: '200',
				end: 'bottom',
				scrub: 'true'
			},
			y: 500
		});
	});
</script>

<section class="projects">
	<div class="title-project">
		<h2>LAST PROJECTS</h2>
	</div>

	<div class="last-projects">
		<div class="first-project">
			<a target="_blank" href="https://buurtcampus-oost-kappa.vercel.app/">
				<img src="plantswap.png" alt="" />
			</a>
			<p>
				"Website voor buurtcampus oost, op de website kun je zien welke stekjes er beschikbaar zijn
				om te ruilen"
			</p>
		</div>

		<div class="second-project">
			<a target="_blank" href="https://squadpage.netlify.app/">
				<img src="squadpage.png" alt="" />
			</a>
			<p>"Op de squadpage kun je zien wie er allemaal in onze squad zit"</p>
		</div>
	</div>
</section>

<style>
	section {
		position: sticky;
		top: 4.3rem;
		background-color: #f0eff4;
		color: #1a535c;
		border-radius: 10px;
		width: 100%;
		height: 90vh;
		padding: var(--padding);
		overflow: hidden;
	}

	h2 {
		font-weight: 200;
	}

	.last-projects {
		display: flex;
		gap: 2rem;
		width: 100%;
		height: 100%;
		padding-top: 2rem;
		padding-bottom: 2rem;
		font-weight: 200;
	}

	.first-project,
	.second-project {
		width: 50%;
		height: 65%;
	}

	.first-project img,
	.second-project img {
		object-fit: cover;
		object-position: top;
		width: 100%;
		height: 100%;
		border-radius: 10px;
	}

	.second-project {
		margin-top: 5rem;
	}
</style>
