<script>
	import LinkedIn from './../lib/images/linkedin.svg';
	export let linkedinUrl = '';
	export let img = '';
	import { fade } from 'svelte/transition';
	import { onMount } from 'svelte';
	let visible = false;
	onMount(() => {
		visible = true;
	});
</script>

{#if visible}
	<div class="card" in:fade={{ duration: 800 }}>
		<img class="image" src={img} alt="portret" />
		<h1><slot name="name" /></h1>
		<p><slot name="description" /></p>
		<div class="link">
			<div class="line"></div>
			<a class="linkedin" href={linkedinUrl}>
				<img src={LinkedIn} alt="LinkedIn Profile" />
			</a>
		</div>
	</div>
{/if}

<style>
	.linkedin {
		width: 2em;
		height: 2em;
	}
	.card {
		max-width: 600px;
		margin: auto;
		display: flex;
		flex-direction: column;
		align-items: center;
		padding: 20px;
		padding-top: 30px;
		border: 1px solid rgba(159, 144, 144, 0.42);

		box-shadow: 2px 2px 6px #ccc;
		box-sizing: border-box;
		border-radius: 20px;
		background-color: rgb(255, 255, 255);
	}
	.image {
		min-width: 200px;
		max-width: 350px;
		box-shadow: 2px 2px 6px #ccc;
		border: 1px solid rgba(159, 144, 144, 0.42);
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
		min-height: 70px;

		text-align: center;
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
		border-top: 2px solid #ccc;

		margin-bottom: 10px;
		border-radius: 100%;
	}
	a {
		width: 100%;
		text-align: center;
	}
</style>
