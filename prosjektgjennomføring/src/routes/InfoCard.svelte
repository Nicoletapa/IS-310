<div class="infoCard">
	<h1><slot name="question" /></h1>
	<p><slot name="info" /></p>
</div>

<style>
	.infoCard {
		display: flex;
		flex-direction: column;
		background-color: white;
		padding: 20px 40px 20px 40px;
		border-radius: 20px;
		margin: auto;
		max-width: 900px;
		margin-top: 20px;
		font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial,
			sans-serif;
		box-shadow: 2px 2px 6px #ccc;
	}
	h1 {
		margin-right: auto;
	}
</style>
