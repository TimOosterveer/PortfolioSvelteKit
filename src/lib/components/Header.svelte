<script>
	import { fly } from 'svelte/transition';
	let navVisible = false;
	let iconBarsVisible = true;

	const toggleNav = () => {
		navVisible = !navVisible;
		iconBarsVisible = !iconBarsVisible;
	};
</script>

<header>
	<div class="menu">
		<p>Oosterveer</p>

		<button aria-label="menu" on:click={toggleNav}>
			{#if iconBarsVisible}
				<i class="fa-solid fa-bars fa-2xl" style="color: #1a202c;" />
			{:else}
				<i class="fa-solid fa-xmark fa-2xl" style="color: #1a202c;" />
			{/if}
		</button>
	</div>
</header>

{#if navVisible}
	<nav id="toggle" class="nav-visible" transition:fly>
		<ul id="links">
			<li><a aria-label="link recente projecten" href="#last-projects">Last Projects</a></li>
			<li><a aria-label="link meer projecten" href="#all-projects">All Projects</a></li>
			<li><a aria-label="link contact overzicht" href="#footer">Contact</a></li>
		</ul>

		<ul id="socials">
			<li>
				<a
					target="_blank"
					aria-label="link naar linkedin"
					href="https://www.linkedin.com/in/tim-oosterveer-a33522124/"
				>
					<i class="fa-brands fa-linkedin fa-2xl" style="color: #1a202c;" />
				</a>
			</li>
			<li>
				<a aria-label="link naar github" target="_blank" href="https://github.com/TimOosterveer">
					<i class="fa-brands fa-github fa-2xl" style="color: #1a202c;" />
				</a>
			</li>
		</ul>
	</nav>
{:else}
	<nav class="toggle nav-hidden" transition:fly />
{/if}

<style>
	header {
		position: absolute;
		background-color: var(--text-color-light);
		color: var(--text-color-dark);
		top: 0;
		left: 0;
		width: 22rem;
		height: 4rem;
		padding: 1rem;
		border-radius: 0 0 10px 0;
		z-index: 2;
	}

	.menu {
		display: flex;
		justify-content: space-between;
	}

	.menu p {
		padding-left: 1rem;
	}

	button {
		border: none;
		cursor: pointer;
	}

	p {
		font-weight: 200;
	}
	nav {
		position: absolute;
		top: 3.4rem;
		background-color: var(--text-color-light);
		border-radius: 0 0 10px 0;
		color: var(--text-color-dark);
		position: absolute;
		width: 22rem;
		height: 22rem;
		padding: var(--padding);
	}

	#toggle {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	ul {
		list-style: none;
		font-weight: 300;
	}

	li {
		padding-top: 1rem;
		transition-duration: 0.2s;
	}

	li:hover {
		transform: translateX(3px);
	}

	a {
		text-decoration: none;
		color: var(--text-color-dark);
	}

	#socials {
		display: flex;

		& li:nth-last-of-type(1) {
			padding-left: 2rem;
		}
	}

	.toggle {
		transition: all 0.1s ease;
	}

	.nav-visible {
		transform: translateY(0);
	}

	.nav-hidden {
		transform: translateY(-100%);
	}

	@media screen and (max-width: 767px) {
		header {
			width: 100%;
			border-radius: 0 0 10px 10px;
		}
		nav {
			height: 15rem;
			border-radius: 0 0 10px 10px;
			width: 100%;
		}
	}
</style>
