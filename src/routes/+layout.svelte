<script>
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<!-- For Fraunces (serif) -->
	<link
		href="https://fonts.googleapis.com/css2?family=Fraunces:wght@600;700&display=swap"
		rel="stylesheet"
	/>
	<!-- For body text replacement for Aktiv Grotesk -->
	<link
		href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

{@render children?.()}

<style lang="scss">
	:global(:root) {
		scroll-behavior: smooth;

		--white: #ffffff;
		--orange: #e56f35;
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
		--fs-22: clamp(22px, 1.14vw, 1.375rem);
		--fs-24: clamp(24px, 1.25vw, 2.5rem);
		--fs-32: clamp(32px, 1.67vw, 3rem);
		--fs-40: clamp(40px, 2.08vw, 2.5rem);
		--fs-44: clamp(44px, 2.23vw, 2.75rem);
		--fs-48: clamp(48px, 2.5vw, 3rem);
		--fs-50: clamp(50px, 2.6vw, 3.125rem);
		--fs-64: clamp(64px, 3.33vw, 4rem);
		--fs-72: clamp(72px, 3.75vw, 4.5rem);
		--fs-150: clamp(150px, 9.81vw, 9.37rem);
	}

	@media (max-width: 1200px) {
		:global(:root) {
			--general-padding: 16rem;
		}
	}

	@media (max-width: 768px) {
		:global(:root) {
			--general-padding: 2rem;
		}
	}

	:global(body) {
		margin: 0;
		background-color: var(--white);
	}

	:global(h1, h2, h3, h4, p, b, a) {
		color: var(--blue);
	}

	:global(h1, h2, h3, h4, h5, h6) {
		font-family: 'Fraunces', serif;
		letter-spacing: 0;
		margin: 0;
	}

	:global(p, b) {
		font-family: 'Roboto', sans-serif;
		letter-spacing: 0;
		margin: 0;
	}

	:global(b) {
		font-weight: 700;
		font-size: var(--fs-22);
		line-height: 160%;
	}

	:global(p) {
		font-weight: 400;
		font-size: var(--fs-22);
		line-height: 160%;
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

	:global(a.underlined) {
		text-decoration: underline;
	}

	:global(a.inverted) {
		color: var(--orange);
	}

	:global(a.inverted:hover) {
		color: var(--light-blue);
	}
</style>
