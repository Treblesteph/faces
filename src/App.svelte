<script>
	export let name;

	import { Images } from "svelte-images";
	const images = [...Array(27)].map((x, i) => ({ src: `https://raw.githubusercontent.com/Treblesteph/faces/main/src/face${i+1}.png`}))
</script>

<main>
	<h1>100 Heads Challenge</h1>
	<p>Based on the wonderful <a href="https://www.pinterest.com/aaldoori/portrait/">Pinterest board</a> and associated challenge put forward by Ahmed Aldoori.</p>

	<Images {images} gutter={5} />
</main>

<style>
	main {
		height: 75vh;
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	#title {
		width: 30%;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>