<script>
	export let product
	export let cta = "Something"
</script>

<li class="card">
	<img src="{product.thumbnail}" alt="placeholder">
	<div class="description">			
		<h2>{product.title}</h2>
		<p>{product.description}</p>
		<a class="button" href>{cta}</a>
	</div>
</li>

<style>
	.card {
		margin-inline: auto;
		background-color: white;
	}
	
	img {
		display: block;
		width: 100%;
		aspect-ratio: 1;
		object-fit: cover;
	}
	
	.description {
		display: grid;
		gap: 1em;
		padding: 1.5em;
	}

	.button {
		padding: 1em;
		background-color: tomato;
		color: white;
		text-align: center;
		text-transform: uppercase;
		font-weight: bold;
		letter-spacing: 1px;
		border: none;
		cursor: pointer;
	}
	
	.button:hover {
		background-color: transparent;
		color: tomato;
		outline: 0.25em solid tomato;
		text-decoration: none;
	}
</style>