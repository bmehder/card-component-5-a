<script>
	export let logo = "Fallback"
</script>

<header>
	<div>		
		<p class="logo">{logo}</p>
		<nav>
			<ul>
				<li><a href>Home</a></li>
				<li><a href>About</a></li>
				<li><a href>Contact</a></li>
			</ul>
		</nav>
	</div>
</header>

<style>
	header {
		background-color: tomato;
		color: white;
	}
	
	div {
		max-width: 64em;
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-inline: auto;
		padding-block: 1.5em;
		padding-inline: 3em;
	}
	
	.logo {
		font-size: 3rem;
		font-weight: bold;
	}
		
	ul {
		display: flex;
		gap: 1.5em;
		list-style: none;
	}
	
	a {
		color: white;
	}
</style>