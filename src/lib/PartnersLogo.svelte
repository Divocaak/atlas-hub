<script>
	export let href;
	export let src;
</script>

<a {href} target="_blank">
	<img {src} alt="logo {src}" />
</a>

<style>
	img {
		max-width: 100%;
		max-height: 80px;
		object-fit: contain;
		display: block;
	}
</style>
