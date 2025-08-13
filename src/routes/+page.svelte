<script>
	import Header from '$lib/Header.svelte';
</script>

<div class="nav">
	<a href="/#program">program</a>
	<a href="/#o-projektu">o projektu</a>
	<a href="/#tvurci">tvůrci</a>
	<a href="/#galerie">galerie</a>
	<a href="/#ochutnavky">ochutnávky</a>
	<a href="/#kontakt">kontakt</a>
</div>

<div class="landing">
	<h1>Atlas podivných hub lesů a strání</h1>
	<h2>Kniha, která se rozrůstá do ulic.</h2>
	<h1>26. 9. - 28. 11. 2025</h1>
	<h2>Vstup zdarma</h2>
</div>

<div class="content-wrapper" id="program">
	<Header heading="program" subheading="Calendarium vium" />
</div>
<div class="content-wrapper" id="o-projektu">
	<Header heading="o projektu" subheading="Mykoversum" subheadingClr="var(--green)" />
	<b>
		V Krumlově vyrostly houby, jaké svět dosud nespatřil.<br />
		Nezrodily se ze spor, ale z imaginace.
	</b>

	<p>
		Atlas podivných hub lesů a strání je výtvarně-literární projekt studentů a pedagogů oboru Užitá
		malba Střední uměleckoprůmyslové školy sv. Anežky České. Propojuje umění, školu a veřejný
		prostor v jedinečný kulturní happening.
	</p>
	<p>
		Po šesti letech tvorby vychází autorská kniha plná fantazijních hub, bizarních názvů, hravých
		textů a ilustrací. A ta ožívá při slavnostním křtu, výstavách a workshopech pro školy - a také v
		unikátní galerii pod širým nebem: polepeném „Houbobusu“ a výtvarně upravené zastávce č. 14.
		Tentokrát galerie nečeká na návštěvníky - vyjíždí sama za nimi.
	</p>
	<p>Rodí se Mykoversum - organismus, který prorůstá městem a zve všechny ke hře.</p>
</div>
<div class="content-wrapper" id="tvurci">
	<Header heading="tvůrci" subheading="Mykonauti" />
	<b>
		Každou houbu někdo objevil ve své fantazii - a zaznamenal ji tak,<br />
		aby mohla růst i ve fantazii druhých.
	</b>
	<p>
		Každá z 88 hub v Atlasu vznikla jako svébytné literárně-výtvarné dílo - od nápadu přes
		tvarosloví až po výtvarné ztvárnění a jazykovou hříčku.
	</p>
	<p>
		Za vznikem knihy a celého projektu stojí 54 studentů a pedagogů oboru Užitá malba SUPŠ sv.
		Anežky České - oboru s více než třicetiletou tradicí, který se mění a roste skrze své lidi.
	</p>
	<p>
		Vizuální identitu vtisklo projektu grafické studio Voala - s respektem k jemnosti, humoru a
		rukopisu každé houby.
	</p>
</div>
<div class="content-wrapper" id="galerie">
	<Header heading="galerie" subheading="Exposio sub caelo" />
	<b>
		Když galerie opustí zdi, i obyčejná jízda autobusem se může proměnit<br />
		ve výpravu do světa imaginace.
	</b>
	<p>
		<b>Houbobus</b> - speciálně polepený linkový autobus - se stal pojízdnou galerií. Spolu s
		výtvarně upravenou <b>zastávkou č. 14</b> na autobusovém nádraží vtahují cestující i kolemjdoucí
		do fantazijního světa Atlasu podivných hub.
	</p>
</div>
<div class="content-wrapper" id="ochutnavky">
	<Header heading="ochutnávky" subheading="Atlas degustatio" />
</div>
<div class="content-wrapper" id="kontakt">
	<Header heading="kontakt a partneří" subheading="Mycelium" />
</div>

<style>
	.nav {
		display: none;
	}

	.landing {
		position: relative;
		background-color: red;
		width: 100%;
		height: 100vh;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.landing h1 {
		color: var(--orange);
	}

	.content-wrapper {
		padding: 0 var(--general-padding);
	}

	#o-projektu {
		background-color: color-mix(in srgb, var(--green) 10%, transparent);
	}

	#ochutnavky {
		background-color: color-mix(in srgb, var(--orange) 10%, transparent);
	}
</style>
