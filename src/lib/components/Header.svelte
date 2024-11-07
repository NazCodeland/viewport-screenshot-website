<script lang="ts">
	import { Camera, Menu, X } from 'lucide-svelte';

	const alternatingWords = ['Screenshot', 'Mockup'];
</script>

<header class="header">
	<div class="logo-section">
		<Camera class="icon" size={24} />
	</div>

	<nav class="desktop-nav">
		<a href="https://youtube.com">Features</a>
		<a href="https://youtube.com">Testimonials</a>
		<a href="https://youtube.com">Pricing</a>
		<a href="https://youtube.com">FAQ</a>
		<a href="https://youtube.com">Contact</a>
	</nav>
</header>

<style lang="postcss">
	.header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: var(--size-3) var(--size-5);
		background: var(--surface-1);
		box-shadow: var(--shadow-1);
		position: sticky;
		top: 0;
		z-index: var(--layer-4);
	}

	.logo-section {
		display: flex;
		align-items: center;
		gap: var(--size-3);
	}

	/* Desktop Navigation */
	.desktop-nav {
		gap: var(--size-5);
	}

	.desktop-nav a {
		color: var(--text-2);
		text-decoration: none;
		font-weight: var(--font-weight-5);
		transition: color 0.2s ease-in-out;
		position: relative;
		padding: var(--size-2);
	}

	.desktop-nav a::after {
		content: '';
		position: absolute;
		bottom: 0;
		left: 0;
		width: 0;
		height: 2px;
		background: var(--brand);
		transition: width 0.2s ease-in-out;
	}

	.desktop-nav a:hover {
		color: var(--text-1);
	}

	.desktop-nav a:hover::after {
		width: 100%;
	}
</style>
