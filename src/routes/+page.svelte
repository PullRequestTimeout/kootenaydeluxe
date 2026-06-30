<script lang="ts">
	import PrimaryButton from "$lib/components/PrimaryButton.svelte";
	import SeoHead from "$lib/components/SeoHead.svelte";
	import Marquee from "svelte-fast-marquee";
	import Carousel from "$lib/components/Carousel.svelte";
</script>

<SeoHead></SeoHead>

<main>
	<section class="hero">
		<h1>Kootenay Deluxe</h1>
		<h2 class="heading-large">Reliable Contracting & Electrical Services in Rossland, British Columbia</h2>
		<p class="body-regular">From small repairs to full-scale projects, we deliver safe, efficient, and code-compliant work you can count on.</p>
		<div>
			<PrimaryButton text="Get a Quote" href="/contact" primary={false} />
			<PrimaryButton text="Call Now" href="tel:+12505052754" primary />
		</div>
	</section>
	<Marquee speed={50} pauseOnHover={false}>
		<div class="icon-heading marquee-item">
			<span class="material-icons">location_on</span>
			<p class="heading-small">Locally owned and operated</p>
		</div>
		<div class="icon-heading marquee-item">
			<span class="material-icons">request_quote</span>
			<p class="heading-small">Free Estimates</p>
		</div>
		<div class="icon-heading marquee-item">
			<span class="material-icons">verified</span>
			<p class="heading-small">Fully Licensed & Insured</p>
		</div>
		<div class="icon-heading marquee-item">
			<span class="material-icons">thumb_up</span>
			<p class="heading-small">Trusted by Our Clients</p>
		</div>
		<div class="icon-heading marquee-item">
			<span class="material-icons">location_on</span>
			<p class="heading-small">Locally owned and operated</p>
		</div>
		<div class="icon-heading marquee-item">
			<span class="material-icons">request_quote</span>
			<p class="heading-small">Free Estimates</p>
		</div>
		<div class="icon-heading marquee-item">
			<span class="material-icons">verified</span>
			<p class="heading-small">Fully Licensed & Insured</p>
		</div>
		<div class="icon-heading marquee-item">
			<span class="material-icons">thumb_up</span>
			<p class="heading-small">Trusted by Our Clients</p>
		</div>
	</Marquee>
	<Carousel />
</main>

<style>
	div.marquee-item {
		margin-right: var(--spacing-m);
		gap: var(--spacing-m);
	}

	:global(.marquee-container) {
		min-height: fit-content;
		overflow: hidden;
	}
</style>
