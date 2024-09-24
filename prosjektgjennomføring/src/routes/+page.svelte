<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import question from '$lib/images/questionMark.jpg';
	import values from '$lib/images/values.jpg';
</script>

<svelte:head>
	<title>Hjem</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section
	style="font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial,
			sans-serif;  "
>
	<h1>
		<span class="welcome">
			<picture>
				<source srcset={welcome} type="image/webp" />
				<img src={welcome_fallback} alt="Welcome" />
			</picture>
		</span>

		<strong>Gruppe 13</strong> <br />
		<span class="text-name">Maria, Nicoleta og Anna</span>
		<br />
		<span class="text-description"
			>Vi er en gruppe engasjerte IT-studenter med et sterkt fokus på samarbeid, innovasjon og
			faglig utvikling.</span
		>
	</h1>
	<selection class="selection-home">
		<div class="card-whoweare">
			<img class="image-who-we-are" src={question} alt="placeholder" />
			<div>
				<h2>Hvem er vi?</h2>
				<p>
					En sammensatt trio med ulike spesialområder og erfaringer som bidrar til et mangfoldig
					perspektiv på alle prosjekter vi tar på oss.
				</p>
			</div>
		</div>
	</selection>
	<selection class="selection-home">
		<h2>Hvordan kan vi bidra?</h2>
		<p>
			Vi tilbyr en unik kombinasjon av ferdigheter og erfaringer som kan tilføre verdi til ethvert
			prosjekt. For å lære mer om hvem vi er, hvordan vi jobber, og hva vi kan gjøre sammen, besøk
			vår «Om oss»-side. Der finner du mer detaljerte informasjoner om våre prosjekter, vår
			kompetanse og lidenskap.
		</p>
	</selection>
	<selection class="selection-home">
		<h2>Hva står vi for?</h2>
		<p>
			Vår misjon er å levere kreative løsninger, oppnå konkrete resultater, og alltid strebe etter
			forbedring. Vi er drevet av kjerneverdier som guider vår tilnærming og beslutningstaking i alt
			vi gjør. Våre prinsipper sørger for at vi alltid er på rett spor og gir oss et solid grunnlag
			for samarbeid og innovasjon. For en dypere forståelse av vår tilnærming og hvordan vi jobber
			sammen, besøk vår «Gruppestrategi»-side.
		</p>
	</selection>

	<selection class="selection-home">
		<h2>Hvem er vi interresert i?</h2>
		<p>
			Vi er på utkikk etter samarbeidspartnere fra næringslivet som er åpne for å dra nytte av vår
			unike kompetanse og perspektiver. Vi søker bedrifter som ønsker å engasjere seg i et spennende
			bachelorprosjekt der vi kan utvikle innovative løsninger på reelle utfordringer. Ved å
			samarbeide med oss, får dere tilgang til friske ideer, grundig analyse, og kreative
			tilnærminger som kan tilføre verdi til deres virksomhet. Dette er en utmerket mulighet for å
			få innsikt og strategiske fordeler, samtidig som vi får praktisk erfaring og bygger videre på
			våre ferdigheter. Hvis dere er interessert i å utforske hvordan vårt samarbeid kan gi
			gjensidig suksess, ser vi frem til å diskutere dette nærmere med dere.
		</p>
		<!-- svelte-ignore a11y-no-redundant-roles -->
		<button class="button-1">Kontakt oss</button>
	</selection>
</section>

<style>
	/* CSS */
	.button-1 {
		background-color: #ea4c89;
		border-radius: 8px;
		border-style: none;
		box-sizing: border-box;
		color: #ffffff;
		cursor: pointer;
		display: inline-block;
		font-family: 'Haas Grot Text R Web', 'Helvetica Neue', Helvetica, Arial, sans-serif;
		font-size: 14px;
		font-weight: 500;
		height: 40px;
		line-height: 20px;
		list-style: none;
		margin: 0;
		outline: none;
		padding: 10px 16px;
		position: relative;
		text-align: center;
		text-decoration: none;
		transition: color 100ms;
		vertical-align: baseline;
		user-select: none;
		-webkit-user-select: none;
		touch-action: manipulation;
	}

	.button-1:hover,
	.button-1:focus {
		background-color: #f082ac;
	}
	h2 {
		font-weight: bold;
		font-size: 1.5rem;
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial,
			sans-serif;
	}

	.selection-home {
		display: flex;
		flex-direction: column;
		background-color: white;
		padding: 20px 40px 20px 40px;
		border-radius: 20px;
		margin: auto;
		max-width: 900px;
		margin-top: 20px;
	}
	.selection-flex-end {
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		width: 90%;
		margin-inline: auto;

		padding: 20px 40px 20px 40px;
	}
	.card-whoweare {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		flex: 0.4;
		gap: 20px;
		min-height: 150px;
		max-width: 900px;
		margin: auto;
	}
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}
	.text-name {
		font-size: 1.2rem;
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial,
			sans-serif;
	}
	.text-description {
		font-size: 1rem;
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial,
			sans-serif;
		width: 100px;
	}

	h1 {
		width: 90%;
	}
	.image-who-we-are {
		width: 200px;
		display: flex;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
