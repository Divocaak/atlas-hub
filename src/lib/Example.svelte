<script>
	export let thumbnail;
	export let label;
	export let desc;
	export let href;
</script>

<!-- svelte-ignore a11y_click_events_have_key_events -->
<!-- svelte-ignore a11y_no_static_element_interactions -->
<div class="wrapper" on:click={() => window.open(href, "_blank")}>
	<div class="thumbnail" style="background-image: url('{thumbnail}');"></div>
	<p class="label">{@html label}</p>
	<p class="desc">{@html desc}</p>
</div>

<style>
	.wrapper {
		display: flex;
		flex-direction: column;
		cursor: pointer;
	}

	.thumbnail {
		aspect-ratio: 1/1;
		/* max-height: 50%; */

		background-position: center;
		background-repeat: none;
		background-clip: border-box;
		background-size: cover;
	}

	p.label {
		color: var(--orange);
		margin-bottom: 0;
		font-family: 'Fraunces', serif;
		font-weight: 600;
		font-size: var(--fs-32);
		line-height: 130%;
		margin-top: 1rem;
	}

	p.desc {
		font-weight: 400;
		font-size: var(--fs-22);
		line-height: 150%;
		margin: 1rem 0;
	}
</style>
