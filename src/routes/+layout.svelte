<script>
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}

<style lang="scss">
	/* @font-face {
		font-family: 'NeueMachina';
		src: url('/fonts/NeueMachina-Light.otf') format('opentype');
		font-weight: 300;
	}

	@font-face {
		font-family: 'NeueMachina';
		src: url('/fonts/NeueMachina-Regular.otf') format('opentype');
		font-weight: 400;
	}

	@font-face {
		font-family: 'NeueMachina';
		src: url('/fonts/NeueMachina-Ultrabold.otf') format('opentype');
		font-weight: 800;
	} */

	:global(:root) {
		scroll-behavior: smooth;

		--white: #ffffff;
		--orange: #E56F35;
		--blue: #303586;
		--light-blue: #6e9ea1;
		--green: #8bac43;
		--purple: #976ea2;
		--pink: #de77a4;

		--general-padding: 22rem;

		/* vw = px value / 19.2 */
		/* rem = px value / 16 */
		--fs-8: clamp(8px, 0.41vw, 0.5rem);
		--fs-12: clamp(12px, 0.625vw, 1rem);
		--fs-14: clamp(14px, 0.73vw, 1.25rem);
		--fs-16: clamp(16px, 0.83vw, 1.5rem);
		--fs-18: clamp(18px, 0.94vw, 1.75rem);
		--fs-20: clamp(20px, 1.04vw, 2rem);
		--fs-24: clamp(24px, 1.25vw, 2.5rem);
		--fs-32: clamp(32px, 1.67vw, 3rem);
		--fs-44: clamp(44px, 2.23vw, 2.75rem);
		--fs-48: clamp(48px, 2.5vw, 3rem);
		--fs-64: clamp(64px, 3.33vw, 4rem);
		--fs-72: clamp(72px, 3.75vw, 4.5rem);
		--fs-150: clamp(150px, 9.81vw, 9.37rem);
	}

	:global(body) {
		margin: 0;
		background-color: var(--white);

		/* font-family: 'NeueMachina', sans-serif;
		letter-spacing: 0px;
		font-style: normal;
		font-variant: normal; */
	}

	:global(h1, h2, h3, h4, p, b, a) {
		color: var(--blue);
		/* line-height: 1.5em;
		letter-spacing: 0.15em; */
	}

	:global(a) {
		transition: all 0.25s ease-in-out;
		text-decoration: none;
	}

	:global(a) {
		color: var(--blue);
	}

	:global(a:hover) {
		color: var(--orange);
	}
</style>
