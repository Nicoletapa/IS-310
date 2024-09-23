<script>
	import InfoCard from '../InfoCard.svelte';
	import Card from './../Card.svelte';
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<h1>Gruppemedlemmene</h1>
<div>
	<div class="card">
		<Card linkedinUrl="https://www.linkedin.com/in/maria-anh-thu-hoang-170530306/">
			<span slot="name">Maria Anh Thu Hoang </span>
			<span slot="description"
				>IT-student | 20 år | Entusiastisk for utvikling og design av teknologi.</span
			>
		</Card>

		<Card linkedinUrl="https://www.linkedin.com/in/nicoleta-pavelescu/">
			<span slot="name">Nicoleta Pavelescu</span>
			<span slot="description"
				>IT-student | 20 år | Fokusert på å skape intuitive digitale løsninger med god
				funksjonalitet.
			</span>
		</Card>
		<Card>
			<span slot="name">Anna Maria Dang</span>
			<span slot="description"
				>IT-student | 20 år | Nysgjerrig på teknologi og klar for å gjøre en forskjell.
			</span>
		</Card>
	</div>
	<div>
		<h1>Møt Vårt Team: Kompetanse og Lidenskap</h1>
		<InfoCard>
			<span slot="question">Maria</span>
			<span slot="info"
				>Maria er en utvikler med engasjement for å gi kreative løsninger med bruk av funksjoner til
				webapplikasjoner gjennom JavaScript. Nysgjerrighet for dynamiske funksjoner og en
				komfortabel brukeropplevelse, gjør henne til en utvikler som setter kvalitet på topp. Maria
				startet rett på høyere utdanning ved Universitetet i Agder i studiet IT og
				informasjonssystemer, etter å ha fullført videregående ved Edvard Munch videregående skole i
				Oslo. I våren 2024, dro hun på utveksling til Sør-Korea, hvor erfaringen fra å ha studert i
				utlandet, har utviklet hennes evner innen kommunikasjon, datautvikling og samskaping.
			</span>
		</InfoCard>
		<InfoCard>
			<span slot="question">Nicoleta</span>
			<span slot="info"
				>Nicoleta er en engasjert frontend-utvikler med en lidenskap for å lage funksjonelle og
				brukervennlige nettsider. Etter å ha fullført videregående skole med toppidrett og realfag,
				begynte hun umiddelbart på høyere utdanning for å fordype seg i webutvikling. Nicoleta
				kombinerer sin tekniske kompetanse med en sterk forståelse for design, og jobber for å skape
				digitale løsninger som er både effektive og attraktive.
			</span>
		</InfoCard>
		<InfoCard>
			<span slot="question">Anna</span>
			<span slot="info"
				>Anna er en kreativ utvikler med en spesiell interesse for webdesign og brukeropplevelse
				(UX). Hun har en sterk estetisk sans og er kjent for å lage intuitive og visuelt tiltalende
				applikasjoner. Etter å ha fullført videregående med International Baccalaureate Diploma
				Programme (IBDP), hvor hun utviklet et solid grunnlag i kritisk tenkning og prosjektledelse,
				begynte Anna umiddelbart på universitetet for å studere IT og informasjonssystemer ved
				Universitetet i Agder. Denne kombinasjonen av analytisk utdanning og universitetsstudier har
				gitt henne en unik evne til å kombinere kreativitet med teknisk innsikt i sine
				utviklingsprosjekter.
			</span>
		</InfoCard>
	</div>
</div>

<style>
	.card {
		display: flex;
		justify-content: center;

		margin: auto;
		gap: 1rem;
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial,
			sans-serif;
	}
	h1 {
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial,
			sans-serif;
	}
	@media (max-width: 800px) {
		.card {
			flex-direction: column;
		}
	}
</style>
