<script>
	import LinkedIn from './../lib/images/linkedin.svg';
	export let linkedinUrl = '';
	export let img = '';
</script>

<div class="card">
	<img src={img} alt="portret" />
	<h1><slot name="name" /></h1>
	<p><slot name="description" /></p>
	<div class="link">
		<div class="line"></div>
		<a class="linkedin" href={linkedinUrl}>
			<img src={LinkedIn} alt="LinkedIn Profile" />
		</a>
	</div>
</div>

<style>
	.linkedin {
		width: 2em;
		height: 2em;
	}
	.card {
		display: flex;
		flex-direction: column;
		align-items: center;

		padding: 20px;
		margin: auto;

		box-sizing: border-box;
		border-radius: 20px;
		box-shadow: 2px 2px 6px #ccc;
	}
	img {
		width: 100%;
		border-radius: 20px;
	}
	h1 {
		margin: 0.5rem 0;
		font-size: 1.5rem;
		font-weight: bold;
		padding: 10px;
	}
	p {
		margin: 0;
		max-width: 400px;
	}
	.link {
		margin-top: 10px;
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.line {
		width: 100%;
		border-top: 1px solid #ccc;
		margin-bottom: 10px;
	}
	a {
		width: 100%;
		text-align: center;
	}
</style>
