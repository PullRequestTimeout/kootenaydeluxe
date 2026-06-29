<script lang="ts">
	import PrimaryButton from "$lib/components/PrimaryButton.svelte";
	import { slide } from "svelte/transition";

	let navMenuOpen = $state(false);
	const toggleNavMenu = () => {
		navMenuOpen = !navMenuOpen;
	};
</script>

<header class="small-screen">
	<a href="/">
		<img class="logo" src="/assets/images/kd-logo-white.png" alt="Kootenay Deluxe Logo" />
	</a>
	<button class="nav-toggle" class:open={navMenuOpen} onclick={toggleNavMenu} aria-label="Toggle navigation menu">
		<span class="hamburger"></span>
		<span class="hamburger"></span>
		<span class="hamburger"></span>
	</button>
	{#if navMenuOpen}
		<nav transition:slide={{ duration: 300, axis: "x" }}>
			<a href="/">Home</a>
			<a href="/about">About</a>
			<a href="/services">Services</a>
			<a href="/work">Work</a>
			<a href="/contact">Contact</a>
			<PrimaryButton text="Get a Quote" href="tel:+12505052754" primary />
		</nav>
	{/if}
</header>
<header class="large-screen">
	<a href="/">
		<img class="logo" src="/assets/images/kd-logo-white.png" alt="Kootenay Deluxe Logo" />
	</a>
	<nav>
		<a href="/">Home</a>
		<a href="/about">About</a>
		<a href="/services">Services</a>
		<a href="/work">Work</a>
		<a href="/contact">Contact</a>
		<PrimaryButton text="Get a Quote" href="tel:+12505052754" primary />
	</nav>
</header>

<style>
	header {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		z-index: 1000;
		padding: 1rem var(--padding-inline);
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
	}

	header nav a {
		color: var(--color-white);
		text-decoration: none;
		position: relative;
		font-family: "Bebas Neue", sans-serif;
		letter-spacing: 0.1em;
		font-size: var(--font-body-m);
	}

	header nav a::after {
		content: "";
		position: absolute;
		bottom: calc(-1 * var(--border-width));
		left: 0;
		display: block;
		width: 0;
		height: var(--border-width);
		background: var(--color-white);
		transition: width 0.3s;
	}

	@media (hover: hover) {
		header nav a:hover::after {
			width: 100%;
		}
	}

	header img.logo {
		width: 8rem;
	}

	header.small-screen {
		position: fixed;
		isolation: isolate;
	}

	header.small-screen::before {
		content: "";
		position: absolute;
		inset: 0;
		background-color: transparent;
		backdrop-filter: blur(1rem);
		-webkit-backdrop-filter: blur(1rem);
		z-index: 0;
		pointer-events: none;
	}

	header.small-screen > * {
		position: relative;
		z-index: 1;
	}

	header.large-screen {
		display: none;
		backdrop-filter: blur(5px);
		-webkit-backdrop-filter: blur(5px);
	}

	/* Small screen nav */
	header.small-screen nav {
		position: absolute;
		top: 100%;
		right: 0;
		width: 100%;
		height: calc(var(--vh, 1vh) * 100 - 6rem);
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 2rem;
		padding: 1rem 0;
		z-index: 2;
		background-color: transparent;
		backdrop-filter: blur(1rem);
		-webkit-backdrop-filter: blur(1rem);
	}

	@media (min-width: 1024px) {
		header.large-screen {
			display: flex;
		}

		header.small-screen {
			display: none;
		}

		header.large-screen nav {
			display: flex;
			gap: 2rem;
			align-items: center;
		}

		header img.logo {
			width: 10rem;
		}
	}

	/* Hamburger menu styles */
	button.nav-toggle {
		background: none;
		border: none;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		width: 2rem;
		height: 1.5rem;
		padding: 0;
	}

	button.nav-toggle .hamburger {
		width: 100%;
		height: 4px;
		background-color: var(--color-white);
		transition: all 0.3s ease-in-out;
	}

	button.nav-toggle.open .hamburger:nth-child(1) {
		transform: rotate(45deg) translate(7px, 7px);
	}

	button.nav-toggle.open .hamburger:nth-child(2) {
		opacity: 0;
	}

	button.nav-toggle.open .hamburger:nth-child(3) {
		transform: rotate(-45deg) translate(7px, -7px);
	}
</style>
