<script>
	import Navbar from '../lib/layout/navbar.svelte';
	import './fonts.css';
</script>

<Navbar />
<slot />

<style global>
	:global(body) {
		margin: 0;
		background-color: var(--color-white);
	}
	:global(*) {
		box-sizing: border-box;
		font-family: Roboto;
	}
	:global(img) {
		object-fit: contain;
	}

	:global(:root) {
		--color-orange: #f49c24;
		--color-orange-light: #f2bb6e;
		--color-cream: #fffcee;
		--color-white: #ffffff;
		--color-blue: #087592;
		--color-dark-blue: #043A49;
		--color-primary: #266d84;
		--color-primary-light: #b1d9e6;
		--color-primary-dark: #0e2933;
		--color-success: #19da43;
		--color-error: #ff0404;
		--color-background: #e5e5e5;
		--color-red: #e8532f;

		--shadow-big-button: -4px -4px 9px -4px rgba(255, 125, 0, 0.8),
			4px 4px 9px -4px rgba(0, 21, 36, 0.8);
		--shadow-big-button-hover: -11px -11px 20px -9px rgba(255, 125, 0, 0.8),
			11px 11px 20px -9px rgba(0, 21, 36, 0.8);
	}
</style>
