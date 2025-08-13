<script>
	export let heading;
	export let subheading;
    export let subheadingClr = "var(--orange)";
</script>

<div class="wrapper">
	<h1>{heading}</h1>
	<h2 style="color: {subheadingClr};">{subheading}</h2>
</div>

<style>
	.wrapper {
		width: 100%;
		
        display: flex;
		flex-direction: column;

		text-align: center;

		padding: 50px 0;
	}

	.wrapper h1 {
		text-transform: uppercase;

		margin: 0;
	}

	.wrapper h2 {
		margin: 0;
	}
</style>
