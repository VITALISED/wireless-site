<script>
 	import wires from '$lib/images/wireless-cat.png';
</script>

<svelte:head>
	<title>#1 site earth real</title>
	<meta name="description" content="hell" />
</svelte:head>

<section>
	<h1>
		Wireless Website
	</h1>

	<picture>
		<img src={wires} alt='wireless cat'/>
	</picture>

	<h2>
		made with <strong>100% organic wireless devices</strong>
	</h2>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	img {
		opacity: 50%;
		margin-top: 5px;
		margin-bottom: 10px;
	}

	h1 {
		width: 100%;
	}

</style>
