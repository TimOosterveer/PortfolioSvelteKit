<script>
	import { gsap } from 'gsap-trial';
	import { onMount } from 'svelte';

	import { ScrollTrigger } from 'gsap/dist/ScrollTrigger';
	gsap.registerPlugin(ScrollTrigger);

  onMount(() => { 
		gsap.from('.wrapper-project1', {
			scrollTrigger:  {
				trigger: '.first-project',
				start: 'top 100',
				end: 'bottom',
				scrub: 'true'
			},
			x: -1500
		});

    gsap.from('.wrapper-project2', {
			scrollTrigger:  {
				trigger: '.wrapper-project1',
				start: 'top 200',
				end: 'bottom',
				scrub: 'true'
			},
			x: 1500
		});
  });

</script>

<section id="all-projects">
	<h2>ALL PROJECTS</h2>
	<div class="wrapper-projects">
		<div class="wrapper-project1">
			<div class="text-about">
				<h3>Abeen Projecten</h3>
				<p>
					Voor Abeen ben ik een website aan het maken voor de projecten die zij maken, dit is
					gekoppeld aan een cms.
				</p>
			</div>

			<div class="logo">
				<a target="_blank" href="https://abeenprojecten.vercel.app/">
					<img src="abeenmac.png" alt="" />
				</a>
			</div>
		</div>

		<div class="wrapper-project2">
			<div class="text-about">
				<h3>Sportiek Reizen</h3>
				<p>
					Voor Sportiek Reizen heb ik een dashboard gemaakt waarin je beschikbaarheid van de
					accommodaties kan zien.
				</p>
			</div>

			<div class="logo">
				<a target="_blank" href="https://outerwear-colt.cyclic.app/">
					<img src="sportiek.png" alt="" />
				</a>
			</div>
		</div>
	</div>
</section>

<style>
	section {
		position: sticky;
		width: 100%;
		height: 100%;
		background-color: var(--background-color);
		border-radius: 10px 10px 0 0;
		padding: var(--padding);
		overflow: hidden;
	}

	h2 {
		position: sticky;
		top: 2rem;
	}

	h2,
	p {
		font-weight: 200;
	}

	.wrapper-projects {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		height: 100%;
		margin-top: 10rem;
	}

	.wrapper-project1,
  .wrapper-project2 {
		display: flex;
		gap: 2rem;
		width: 80vw;
		margin-bottom: 10rem;
	}

	.logo {
		width: 55vw;
		height: 35vw;
	}

	a {
		text-decoration: none;
	}

	.text-about {
		display: flex;
		flex-direction: column;
		justify-content: center;
		width: 20vw;

		& h3 {
			font-size: 2rem;
			margin-bottom: var(--padding);
		}
	}

	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: top;
	}


	@media screen and (max-width: 767px) {
		.text-about {
			width: 100%;
		}

		.wrapper-project1,
		.wrapper-project2 {
			display: flex;
			flex-direction: column;
			width: 100%;
		}

		p {
			width: 100%;
		}
	}
</style>
