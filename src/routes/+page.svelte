<div class="nav">
	<a href="/#o-projektu">O projektu</a>
	<a href="/#tvurci">Tvůrci</a>
	<a href="/#program">Program</a>
	<a href="/">Galerie</a>
	<a href="/">Audio ukázky</a>
	<a href="/">Kontakt</a>
</div>

<div class="landing">
	<h1>Atlas podivných hub lesů a strání</h1>
	<h2>Kniha, která se rozrůstá do ulic.</h2>
	<h1>26. 9. - 28. 11. 2025</h1>
	<h2>Vstup zdarma</h2>
	<div class="cta-wrapper">
		<a href="/" class="cta-button">Objevte příběh</a>
		<a href="/" class="cta-button">Navštivte galerii</a>
		<a href="/" class="cta-button">Poslechnětě si houby</a>
	</div>
</div>

<div class="content-wrapper">
	<h1 class="label" id="o-projektu">O projektu</h1>
	<div class="two-panels-wrapper">
		<div class="panel">
			<p>
				<b>
					Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse hendrerit metus quis
					massa tincidunt pulvinar. Duis rutrum ac arcu non vestibulum. Curabitur non mollis nulla.
					Proin ac lobortis lectus, nec placerat lorem. Phasellus eget tincidunt magna, ac fermentum
					leo. Mauris hendrerit eros quis diam efficitur, at vulputate mi finibus.
				</b>
			</p>
		</div>
		<div class="panel">
			<p>
				Curabitur dapibus lacus id mattis consectetur. Etiam aliquet nisi quam, vitae faucibus sem
				sodales eget. Fusce in eleifend metus, quis laoreet ex. Ut luctus, sem quis accumsan ornare,
				orci lectus laoreet erat, vulputate elementum odio lectus at ligula. Cras iaculis, mi eget
				fermentum dignissim, elit tortor gravida sem, eget cursus ipsum sem sit amet lacus. Duis leo
				dolor, suscipit sed mattis quis, cursus eu mi. Vestibulum convallis fermentum mi, ut laoreet
				eros eleifend nec. Curabitur mattis, risus in ultricies volutpat, purus ligula pulvinar ex,
				et hendrerit odio dui at massa. Ut rhoncus interdum nisl eu porttitor. Duis mattis egestas
				auctor.
			</p>
		</div>
	</div>

	<h1 class="label" id="tvurci">Tvůrci</h1>
	<div class="two-panels-wrapper v-centered">
		<div class="panel bg-image" style="background-image: url('/placeholder.jpeg')"></div>
		<div class="panel">
			<p>
				Curabitur dapibus lacus id mattis consectetur. Etiam aliquet nisi quam, vitae faucibus sem
				sodales eget. Fusce in eleifend metus, quis laoreet ex. Ut luctus, sem quis accumsan ornare,
				orci lectus laoreet erat, vulputate elementum odio lectus at ligula.
			</p>
		</div>
	</div>
	<div class="two-panels-wrapper v-centered">
		<div class="panel">
			<p>
				Curabitur dapibus lacus id mattis consectetur. Etiam aliquet nisi quam, vitae faucibus sem
				sodales eget. Fusce in eleifend metus, quis laoreet ex. Ut luctus, sem quis accumsan ornare,
				orci lectus laoreet erat, vulputate elementum odio lectus at ligula.
			</p>
		</div>
		<div class="panel bg-image" style="background-image: url('/placeholder.jpeg')"></div>
	</div>
	<div class="two-panels-wrapper v-centered">
		<div class="panel bg-image" style="background-image: url('/placeholder.jpeg')"></div>
		<div class="panel">
			<p>
				Curabitur dapibus lacus id mattis consectetur. Etiam aliquet nisi quam, vitae faucibus sem
				sodales eget. Fusce in eleifend metus, quis laoreet ex. Ut luctus, sem quis accumsan ornare,
				orci lectus laoreet erat, vulputate elementum odio lectus at ligula.
			</p>
		</div>
	</div>

    <h1 class="label" id="program">Program</h1>
</div>

<style>
	.nav {
		position: fixed;
		top: 0;
		width: 100%;
		padding: 0.5rem 0;

		display: flex;
		flex-direction: row;
		justify-content: center;
		gap: 2rem;

		box-shadow: 0px 5px 10px 0px rgba(0, 0, 0, 0.75);
		-webkit-box-shadow: 0px 5px 10px 0px rgba(0, 0, 0, 0.75);
		-moz-box-shadow: 0px 5px 10px 0px rgba(0, 0, 0, 0.75);

		background-color: var(--white);
		z-index: 1000;
	}

	.landing {
		position: relative;
		background-color: red;
		width: 100%;
		height: 95vh;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.cta-wrapper {
		display: flex;
		flex-direction: row;
		width: 100%;
		justify-content: space-evenly;
	}

	.cta-button {
		background-color: var(--red);
		color: var(--white);

		padding: 1rem 2rem;
		border-radius: 2rem;

		transition: all 0.25s ease-in-out;
	}

	.cta-button:hover {
		background-color: var(--white);
		color: var(--red);
	}

	.content-wrapper {
		padding: 0 var(--general-padding);
	}

	.label {
		width: 100%;
		text-align: center;
	}

	.two-panels-wrapper {
		width: 100%;
		display: flex;
		flex-direction: row;
		gap: 2rem;
	}

	.two-panels-wrapper.v-centered {
		align-items: center;
	}

	.two-panels-wrapper .panel {
		width: 50%;
	}

	.two-panels-wrapper .panel.bg-image {
		background-position: center;
		background-repeat: no-repeat;
		background-size: cover;
		min-height: 350px;
	}
</style>
