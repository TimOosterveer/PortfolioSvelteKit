<script>
	import { gsap } from 'gsap';
	import { onMount } from 'svelte';
</script>

<section>
	<div class="info-me">
		<h1>TIM OOSTERVEER</h1>
		<p class="p">Student Frontend Development</p>
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
		overflow: hidden;
	}
	
	h1 {
		overflow: hidden;
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

	@media screen and (max-width: 767px) {
		section {
			width: 100%;
			height: 50vh;
		}

		h1 {
			font-size: 2rem;
			height: 10vh;
		}

		p {
			text-align: left;
		}
	}
</style>
