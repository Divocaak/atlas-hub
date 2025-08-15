<script>
	export let date;
	export let label;
	export let desc;
	export let isLast = false;
</script>

<div class="wrapper" class:last={isLast}>
	<h1 class="date">{@html date}</h1>
	<div class="content">
		<h1>{@html label}</h1>
		<p>{@html desc}</p>
		<a
			href="https://www.knih-ck.cz/cz/mestska-knihovna-cesky-krumlov/"
			target="_blank"
			class="underlined inverted"
		>
			Městská knihovna v Českém Krumlově
		</a>
	</div>
</div>

<style>
	.wrapper {
		display: flex;
		flex-direction: row;
		width: 100%;

		border-top: 1.5px solid var(--orange);

		padding: 2rem 0;
	}

	.last {
		border-bottom: 1.5px solid var(--orange);
	}

	h1 {
		font-weight: 600;
		font-size: 32px;
		line-height: 120%;
	}

	.date {
		min-width: 35%;
		color: var(--orange);
	}

	.content {
		display: flex;
		flex-direction: column;
	}

	.content p {
		font-weight: 400;
		font-size: 18px;
		line-height: 150%;
        margin: 1rem 0;
	}

	.content a {
		font-family: 'Fraunces', serif;
		font-weight: 400;
		font-size: 18px;
		line-height: 120%;
	}
</style>
