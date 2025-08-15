<script>
	import { fade } from 'svelte/transition';

	let open = false;
	function toggleMenu() {
		open = !open;
	}
</script>

<div class="btn-wrapper">
	<!-- Hamburger Button -->
	<button class="hamburger" on:click={toggleMenu} aria-label="Menu">
		<span class:open></span>
		<span class:open></span>
		<span class:open></span>
	</button>
</div>

<!-- Fullscreen Overlay -->
{#if open}
	<nav class="overlay" transition:fade={{ duration: 200 }}>
		<a href="/#program" on:click={() => (open = false)}>program</a>
		<a href="/#o-projektu" on:click={() => (open = false)}>o projektu</a>
		<a href="/#tvurci" on:click={() => (open = false)}>tvůrci</a>
		<a href="/#galerie" on:click={() => (open = false)}>galerie</a>
		<a href="/#ochutnavky" on:click={() => (open = false)}>ochutnávky</a>
		<a href="/#kontakt" on:click={() => (open = false)}>kontakt</a>
	</nav>
{/if}

<style>
	.btn-wrapper {
		position: fixed;
		z-index: 1001;

		background-color: color-mix(in srgb, var(--white) 90%, transparent);
		width: calc(100% - 6rem);
		height: fit-content;

		display: flex;
		flex-direction: row-reverse;

		padding: 1rem 3rem;

		/* position: relative; */
		outline: 3rem solid transparent; /* space for the "border" */
		outline-offset: -3rem; /* keeps it snug against the element */
		box-shadow: 0 -3rem 0 0 transparent; /* fallback */
	}

	.btn-wrapper::before {
		content: '';
		position: absolute;
		bottom: -3rem; /* same as outline thickness */
		left: 0;
		width: 100%;
		height: 3rem;
		background: linear-gradient(
			to bottom,
			color-mix(in srgb, var(--white) 90%, transparent),
			transparent
		);
	}

	/* Hamburger button */
	.hamburger {
		position: relative;

		width: 2rem;
		height: 2rem;

		display: flex;
		flex-direction: column;
		justify-content: space-between;

		background: none;
		border: none;
		cursor: pointer;
		padding: 0;
	}

	.hamburger span {
		display: block;
		height: 3px;
		width: 100%;
		background: var(--blue);
		transition:
			transform 0.3s ease,
			opacity 0.3s ease;
	}

	/* Animate into X */
	.hamburger span.open:nth-child(1) {
		transform: translateY(14px) rotate(45deg);
	}
	.hamburger span.open:nth-child(2) {
		opacity: 0;
	}
	.hamburger span.open:nth-child(3) {
		transform: translateY(-13.5px) rotate(-45deg);
	}

	/* Fullscreen overlay */
	.overlay {
		position: fixed;
		inset: 0;
		background-color: color-mix(in srgb, var(--white) 95%, transparent);

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;

		z-index: 1000;
	}

	.overlay a {
		font-family: 'Fraunces', serif; /* via Google Fonts */
		font-weight: 600; /* SemiBold */
		font-size: 34px;
		line-height: 270%;
		text-align: center;
		text-transform: uppercase;
		vertical-align: middle;
		letter-spacing: 0;
	}
</style>
