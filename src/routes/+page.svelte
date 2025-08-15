<script>
	import Carousel from '$lib/Carousel.svelte';
	import Event from '$lib/Event.svelte';
	import Example from '$lib/Example.svelte';
	import Header from '$lib/Header.svelte';
	import Navbar from '$lib/Navbar.svelte';
</script>

<Navbar />

<div class="landing">
	<h1>Atlas<br />podivných&nbsp;hub<br />lesů&nbsp;a&nbsp;strání</h1>
	<h2>Kniha,&nbsp;která se rozrůstá do ulic.</h2>
	<h1>26. 9. - 28. 11. 2025</h1>
	<h2>Vstup zdarma</h2>
</div>

<div class="content-wrapper" id="program">
	<Header heading="program" subheading="Calendarium vium" />
	<Event
		date="26. 9. od 14:00"
		label="Slavnostní křest knihy<br>a vernisáž ilustrací"
		desc="Za přítomnosti autorů, hudby i hub."
	/>
	<Event
		date="26. 9. - 28. 11."
		label="Výstava ilustrací knihy"
		desc="Imaginární houby zapouští kořeny mezi regály knih."
	/>
	<Event
		date="říjen - listopad"
		label="Výtvarné workshopy<br>pro žáky základních škol<br>a výtvarná soutěž."
		desc="Téma: Houba z fantazie<br>
				Lektorky: studentky SUPŠ<br>
				a pedagožka Věra Chovancová<br>
				Na workshopy je třeba<br>
				se předem přihlásit.<br>"
	/>
	<Event
		date="14. 11. - 28. 11."
		label="Výstava dětských výtvarných<br>a soutěžních prací z&nbsp;workshopů"
		desc="Imaginární houby rozšiřují své řady."
		isLast={true}
	/>
	<div class="wrapper">
		<b>
			Když kniha prorůstá městem, začnou se dít věci.<br />
			Sledujte, kdy a kde se Mykoversum zjeví příště.
		</b><br />
		<a
			href="https://www.knih-ck.cz/cz/mestska-knihovna-cesky-krumlov/"
			target="_blank"
			class="underlined inverted"
		>
			Městská knihovna v Českém Krumlově
		</a>
		<p>
			Výstavy jsou přístupné během
			<a
				href="https://www.knih-ck.cz/cz/provozni-doba-mestske-knihovny-v-ceskem-krumlove/"
				target="_blank"
				class="underlined"
			>
				otevírací doby městské knihovny
			</a>
		</p>
		<b style="color:var(--orange);">Vstup zdarma</b>
	</div>
</div>
<div class="content-wrapper" id="o-projektu">
	<Header heading="o&nbsp;projektu" subheading="Mykoversum" subheadingClr="var(--green)" />
	<img src="/about.jpg" alt="about" />
	<div class="wrapper">
		<b>
			V Krumlově vyrostly houby, jaké svět dosud nespatřil.<br />
			Nezrodily se ze spor, ale z imaginace.
		</b>
		<p>
			Atlas podivných hub lesů a strání je výtvarně-literární projekt studentů a pedagogů oboru
			Užitá malba Střední uměleckoprůmyslové školy sv. Anežky České. Propojuje umění, školu a
			veřejný prostor v jedinečný kulturní happening.
		</p>
		<p>
			Po šesti letech tvorby vychází autorská kniha plná fantazijních hub, bizarních názvů, hravých
			textů a ilustrací. A ta ožívá při slavnostním křtu, výstavách a workshopech pro školy - a také
			v unikátní galerii pod širým nebem: polepeném „Houbobusu“ a výtvarně upravené zastávce č. 14.
			Tentokrát galerie nečeká na návštěvníky - vyjíždí sama za nimi.
		</p>
		<p>Rodí se Mykoversum - organismus, který prorůstá městem a zve všechny ke hře.</p>
	</div>
</div>
<div class="content-wrapper" id="tvurci">
	<Header heading="tvůrci" subheading="Mykonauti" />
	<div class="imgs-wrapper">
		<div class="bg-img" style="background-image: url('/creators/0.jpg');"></div>
		<div class="bg-img" style="background-image: url('/creators/1.jpg');"></div>
		<div class="bg-img" style="background-image: url('/creators/2.jpg');"></div>
		<div class="bg-img" style="background-image: url('/creators/3.jpg');"></div>
		<div class="bg-img" style="background-image: url('/creators/4.jpg');"></div>
		<div class="bg-img" style="background-image: url('/creators/5.jpg');"></div>
	</div>
	<div class="carousel-wrapper">
		<Carousel
			slides={[
				'/creators/0.jpg',
				'/creators/1.jpg',
				'/creators/2.jpg',
				'/creators/3.jpg',
				'/creators/4.jpg',
				'/creators/5.jpg'
			]}
			aspectRatio={1 / 1}
			slideWidth={100}
		/>
	</div>
	<div class="wrapper">
		<b>
			Každou houbu někdo objevil ve své fantazii - a zaznamenal ji tak, aby mohla růst i ve fantazii
			druhých.
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
</div>
<div class="content-wrapper" id="galerie">
	<Header heading="galerie" subheading="Exposio sub caelo" />
	<div class="wrapper">
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
</div>
<Carousel slides={['/gallery/0.jpg', '/gallery/1.jpg']} />
<div class="content-wrapper" id="ochutnavky">
	<Header heading="ochutnávky" subheading="Atlas degustatio" />
	<b>Ochutnávka, která nesytí žaludek, ale představivost.</b>
	<div class="wrapper">
		<Example
			thumbnail="/examples/0.jpg"
			label="Parohlíz&nbsp;lupadřivý"
			desc="Parochialituberi&nbsp;foliesis<br>Daniel Hinšt (autor ilustrace)"
			href="https://www.youtube.com/watch?v=p7SZ0xqDimQ"
		/>
		<Example
			thumbnail="/examples/1.jpg"
			label="Mocho&nbsp;mů(r)ka"
			desc="Mocho&nbsp;pléna muscárum<br>Natálie Herzová"
			href="https://www.youtube.com/watch?v=b-MWUdJOMt8"
		/>
		<Example
			thumbnail="/examples/2.jpg"
			label="Lucerník&nbsp;Bažinný"
			desc="Paludis&nbsp;laternae<br>Zuzana Boháčová"
			href="https://www.youtube.com/watch?v=oC3P0qANRho"
		/>
		<Example
			thumbnail="/examples/3.jpg"
			label="Měsíčnice&nbsp;Tajemná"
			desc="Talnacuum&nbsp;lunas<br>Františka Boková"
			href="https://www.youtube.com/watch?v=6ymVWsJ4YyQ"
		/>
	</div>
</div>
<div class="content-wrapper" id="kontakt">
	<Header heading="kontakt a partneří" subheading="Mycelium" />
	<div class="wrapper">
		<b>
			Žádná houba nevyroste bez podhoubí&nbsp;-&nbsp;to naše vytváří vztahy, důvěra<br />
			a radost ze společného tvoření.
		</b>

		<p>
			<b>Koordinace projektu</b><br />
			MgA. Věra Chovancová, pedagožka SUPŠ sv. Anežky České<br />
			<a class="underlined" href="mailto:vera.chovancova@supsck.cz">vera.chovancova@supsck.cz</a><br
			/>
			<a class="underlined" href="tel:+420721832193">+420&nbsp;721&nbsp;832&nbsp;193</a>
		</p>
		<p>
			Tento projekt vyrostl z&nbsp;podhoubí představ, vztahů a tvořivosti. Každý, kdo přispěl svým
			vláknem&nbsp;-&nbsp;nápadem, ilustrací, trpělivostí, podporou či
			přítomností&nbsp;-&nbsp;pomohl tomuto organismu zakořenit, vyrůst… a růst dál. Děkujeme všem,
			kdo byli a zůstávají jeho součástí, včetně našich partnerů.
		</p>
	</div>
	<div class="partners">
		<img src="/partners/0.png" alt="partners logos" />
		<img src="/partners/1.png" alt="partners logos" />
		<img src="/partners/2.png" alt="partners logos" />
		<img src="/partners/3.png" alt="partners logos" />
	</div>
</div>
<div class="content-wrapper" id="footer">
	<h1>Upozornění</h1>
	<p class="warning">
		Veškeré houby zobrazené na tomto webu jsou smyšlené. Jakákoli jejich podobnost s reálnými druhy
		je čistě náhodná&nbsp;-&nbsp;nebo vysněná.
	</p>
	<p class="footer">
		&copy; 2025 Atlas hub - MgA. Věra Chovancová | Design:&nbsp;
		<a href="https://www.voala.cz/" target="_blank" class="underlined">VOALA</a>
		| Tvorba webu:&nbsp;
		<a href="https://divokyvojtech.cz/" terget="_blank" class="underlined">Divoký Vojtěch</a><br />
		<a href="/info" target="_blank" class="underlined">
			Zpracování osobních údajů | Zásady použití cookies
		</a>
	</p>
</div>

<style>
	img {
		width: 100%;
		height: auto;
	}

	.landing {
		position: relative;
		width: 100%;
		height: 100vh;

		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;

		background-image: url('/landing/desktop.jpg');
		background-position: center;
		background-repeat: none;
		background-clip: border-box;
		background-size: cover;
		background-attachment: fixed;
	}

	.landing h1 {
		color: var(--orange);
		font-weight: 600;
		font-size: var(--fs-72);
		line-height: 100%;
		text-align: center;
		text-transform: uppercase;
	}

	.landing h2 {
		font-weight: 700;
		font-size: var(--fs-40);
		line-height: 120%;
		text-align: center;
	}

	.content-wrapper {
		padding: 0 var(--general-padding);
		padding-bottom: 4rem;
	}

	.content-wrapper#program {
		display: flex;
		flex-direction: column;
		align-items: center;

		position: relative;
		outline: 2rem solid transparent; /* space for the "border" */
		outline-offset: -2rem; /* keeps it snug against the element */
		box-shadow: 0 -2rem 0 0 transparent; /* fallback */
	}

	.content-wrapper#program::before {
		content: '';
		position: absolute;
		top: -2rem; /* same as outline thickness */
		left: 0;
		width: 100%;
		height: 2rem;
		background: linear-gradient(to top, var(--white), transparent);
	}

	.content-wrapper#program .wrapper {
		padding-top: 5rem;

		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.content-wrapper#program .wrapper a.underlined.inverted {
		font-family: 'Fraunces', serif;
		font-weight: 400;
		font-size: var(--fs-18);
		line-height: 120%;
	}

	.content-wrapper#o-projektu {
		background-color: color-mix(in srgb, var(--green) 10%, transparent);
	}

	.content-wrapper#o-projektu .wrapper,
	.content-wrapper#tvurci .wrapper,
	.content-wrapper#galerie .wrapper,
	.content-wrapper#kontakt .wrapper {
		display: flex;
		flex-direction: column;
		gap: 3rem;

		margin-top: 4rem;
	}

	.content-wrapper#tvurci .imgs-wrapper {
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr 1fr 1fr;
		gap: 0.5rem;
	}

	.content-wrapper#tvurci .carousel-wrapper {
		display: none;
	}

	.content-wrapper#tvurci .imgs-wrapper .bg-img {
		aspect-ratio: 1/1;

		background-position: center;
		background-repeat: none;
		background-clip: border-box;
		background-size: cover;
	}

	.content-wrapper#ochutnavky {
		background-color: color-mix(in srgb, var(--orange) 10%, transparent);
	}

	.content-wrapper#ochutnavky b {
		display: block;
		text-align: center;
		margin-bottom: 4rem;
	}

	.content-wrapper#ochutnavky .wrapper {
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr 1fr;
		gap: 2rem;
	}

	.content-wrapper#kontakt .partners {
		display: grid;
		grid-template-columns: 1fr 1fr;
		grid-template-rows: 1fr 1fr;
		gap: 2rem;
		margin: 6rem 0;
	}

	.content-wrapper#footer {
		background-color: color-mix(in srgb, var(--light-blue) 10%, transparent);
		padding-top: 6rem;
		padding-bottom: 6rem;
	}

	.content-wrapper#footer .warning {
		font-weight: 400;
		font-size: var(--fs-22);
		line-height: 150%;
		margin: 2rem 0;
	}

	.content-wrapper#footer .footer {
		font-weight: 400;
		font-size: var(--fs-12);
		line-height: 150%;
	}

	@media (max-width: 768px) {
		.landing {
			background-image: url('/landing/mobile.jpg');
		}

		.landing h1 {
			font-size: var(--fs-32);
		}

		.landing h2 {
			font-size: var(--fs-22);
		}

		.content-wrapper#program .wrapper {
			align-items: start;
		}

		.content-wrapper#tvurci .imgs-wrapper {
			display: none;
		}
		.content-wrapper#tvurci .carousel-wrapper {
			display: block;
		}

		.content-wrapper#ochutnavky .wrapper,
		.content-wrapper#kontakt .partners {
			display: flex;
			flex-direction: column;
		}
	}
</style>
