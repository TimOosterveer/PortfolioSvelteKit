<script>
	import { gsap } from 'gsap-trial';
	import { onMount } from 'svelte';
</script>

<section>
	<div class="info-me">
		<h1>TIM OOSTERVEER</h1>
		<p class="p">Student Frontend Developer</p>
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
