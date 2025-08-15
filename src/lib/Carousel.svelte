<script>
	export let showControls = false;
	export let showIndicators = false;
	export let slides;

	let current = 0;

	let startX = 0;
	let deltaX = 0;
	let isDragging = false;

	const slideWidth = 75;

	// --- touch events ---
	function handleTouchStart(e) {
		startX = e.touches[0].clientX;
		isDragging = true;
		deltaX = 0;
	}
	function handleTouchMove(e) {
		if (!isDragging) return;
		deltaX = e.touches[0].clientX - startX;
	}
	function handleTouchEnd() {
		endDrag();
	}

	// --- mouse events ---
	function handleMouseDown(e) {
		startX = e.clientX;
		isDragging = true;
		deltaX = 0;
		window.addEventListener('mousemove', handleMouseMove);
		window.addEventListener('mouseup', handleMouseUp);
	}
	function handleMouseMove(e) {
		if (!isDragging) return;
		deltaX = e.clientX - startX;
	}
	function handleMouseUp() {
		endDrag();
		window.removeEventListener('mousemove', handleMouseMove);
		window.removeEventListener('mouseup', handleMouseUp);
	}

	// --- shared end logic ---
	function endDrag() {
		if (!isDragging) return;
		isDragging = false;

		if (Math.abs(deltaX) > 50) {
			if (deltaX > 0) prev();
			else next();
		}
		deltaX = 0;
	}

	const next = () => (current = (current + 1) % slides.length);
	const prev = () => (current = (current - 1 + slides.length) % slides.length);
</script>

<div class="carousel">
	<!-- svelte-ignore a11y_no_static_element_interactions -->
	<div
		class="slides"
		on:touchstart={handleTouchStart}
		on:touchmove={handleTouchMove}
		on:touchend={handleTouchEnd}
		on:mousedown={handleMouseDown}
		style="
			transform: translateX(calc({-current * slideWidth}% + {deltaX}px));
			transition: {isDragging ? 'none' : 'transform 0.3s ease'};
		"
	>
		{#each slides as slide}
			<div class="slide" style="background-image: url('{slide}');"></div>
		{/each}
	</div>

	{#if showControls}
		<button class="control left" on:click={prev}>‹</button>
		<button class="control right" on:click={next}>›</button>
	{/if}

	{#if showIndicators}
		<div class="indicators">
			{#each slides as _, i}
				<div class="dot {i === current ? 'active' : ''}"></div>
			{/each}
		</div>
	{/if}
</div>

<style>
	.carousel {
		position: relative;
		overflow: hidden;
		width: 100%;
		/* max-width: 600px; */
		margin: auto;
		user-select: none;

        margin-bottom: 100px;
	}

	.slides {
		display: flex;
		cursor: grab;
	}

	.slide {
		flex: 0 0 75%;
		aspect-ratio: 16/9;

		touch-action: pan-y; /* allow vertical scroll */

		background-position: center;
		background-repeat: none;
		background-clip: border-box;
		background-size: cover;

		margin: 0 2rem;
	}

	.control {
		position: absolute;
		top: 50%;
		transform: translateY(-50%);
		background: rgba(0, 0, 0, 0.5);
		color: white;
		border: none;
		font-size: 2rem;
		cursor: pointer;
		padding: 0.3em 0.6em;
	}
	.control.left {
		left: 10px;
	}
	.control.right {
		right: 10px;
	}

	.indicators {
		position: absolute;
		bottom: 10px;
		left: 50%;
		transform: translateX(-50%);
		display: flex;
		gap: 8px;
	}

	.dot {
		width: 12px;
		height: 12px;
		border-radius: 50%;
		background: rgba(255, 255, 255, 0.5);
	}
	.dot.active {
		background: white;
	}
</style>
