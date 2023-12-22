<script>
	import Header from '../lib/layout/header.svelte';
	import Footer from '$lib/layout/footer.svelte';
</script>

<Header />
<slot />
<Footer />

<style global>
	:global(body) {
		margin: 0;
		background-color: var(--color-background);
		font-size: 16px;
	}
	:global(*) {
		box-sizing: border-box;
		font-family: 'Noto Sans', sans-serif;
	}
	:global(img) {
		object-fit: contain;
	}

	:global(:root) {
		--color-background: #e5e5e5;
		--color-primary: #000000;
		--container: 32px;
	}
	@media (min-width: 1024px) {
		:global(:root) {
			--container: 128px;
		}
	}
	@media (min-width: 1600px) {
		:global(:root) {
			--container: calc((100% - 1000)/ 2);
		}
	}
</style>
