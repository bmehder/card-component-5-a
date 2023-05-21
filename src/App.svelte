<script>
	import Header from './Header.svelte'
	import PageTitle from './PageTitle.svelte'
	import Card from './Card.svelte'
	import Footer from './Footer.svelte'
	
	let products = []
	
	fetch('https://dummyjson.com/products?limit=9')
		.then(res => res.json())
		.then(json => products = json.products)
  
	$: console.log(products)
</script>

<Header logo="Logo" />

<main>
	<PageTitle title="Store" />	

	<ul>
		{#each products as product}
			<Card {product} cta="Buy Now" />
		{/each}
	</ul>
</main>

<Footer text="John Doe." />

<style>
	ul {
		max-width: 64em;
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(16em, 1fr));
		gap: 3em;
		margin-inline: auto;
		padding: 3em;
		line-height: 1.5;
	}
	
	:global(*) {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
/* 		outline: 1px solid lime; */
	}
	
	:global(body) {
		padding: 0;
		background-color: black;
	}
</style>