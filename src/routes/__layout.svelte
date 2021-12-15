<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main class="container">
	<slot />
</main>

<footer>
	<p>visit <a href="https://docs.onflow.org">docs.onflow.org</a> to learn more.</p>
</footer>

<style>

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
