<script lang="ts">
	import PrimaryButton from "$lib/components/PrimaryButton.svelte";
	import SeoHead from "$lib/components/SeoHead.svelte";
	import Marquee from "svelte-fast-marquee";
	import Carousel from "$lib/components/Carousel.svelte";
	import WhyChooseUs from "$lib/components/WhyChooseUs.svelte";
	import RecentProjects from "$lib/components/RecentProjects.svelte";
	import FeedbackCarousel from "$lib/components/FeedbackCarousel.svelte";
	import FAQ from "$lib/components/FAQ.svelte";
	import { homeFaqs } from "$lib/data/faqs.js";
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
	<section class="services">
		<div class="services-text">
			<div class="services-heading">
				<h2 class="heading-small">Our Services</h2>
				<h3 class="heading-large">Electrical & Contracting Services for Homes and Businesses</h3>
				<p class="body-regular">
					Electrical upgrades, renovations, repairs, and finishing work – quality craftsmanship backed by dependable service.
				</p>
			</div>
			<div class="services-list">
				<div class="service-item">
					<div class="icon-heading">
						<span class="material-icons">flash_on</span>
						<p class="heading-small">Electrical Services</p>
					</div>
					<p class="body-regular">Installations, repairs, panel upgrades, lighting, troubleshooting, and code-compliant electrical work.</p>
				</div>
				<div class="service-item">
					<div class="icon-heading">
						<span class="material-icons">construction</span>
						<p class="heading-small">General Contracting</p>
					</div>
					<p class="body-regular">Basement suites, bathroom renovations, siding, finishing work, repairs, and home improvement projects.</p>
				</div>
			</div>
			<PrimaryButton text="Explore All Services" href="/services" primary />
		</div>
		<div class="services-image">
			<img src="/assets/images/services-image.jpg" alt="Electrical and Contracting Services" />
		</div>
	</section>
	<WhyChooseUs />
	<RecentProjects />
	<FeedbackCarousel />
	<FAQ faqs={homeFaqs} />
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

	/* Services */
	section.services {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-m);
	}

	section.services div.services-text h2 {
		color: var(--color-primary);
	}

	section.services div.services-text,
	section.services div.services-heading,
	section.services div.services-list {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-m);
	}

	section.services div.services-heading {
		gap: var(--spacing-xs);
	}

	@media (min-width: 640px) {
		section.services,
		section.services div.services-text {
			gap: var(--spacing-l);
		}

		section.services div.services-list {
			display: grid;
			grid-template-columns: 1fr 1fr;
			gap: var(--spacing-l);
		}
	}

	@media (min-width: 1024px) {
		section.services {
			grid-template-columns: 1fr 1fr;
			gap: var(--spacing-xl);
		}

		section.services div.services-text {
			gap: var(--spacing-l);
		}

		section.services div.services-image {
			display: flex;
			align-items: center;
			justify-content: center;
		}
	}

	@media (min-width: 1280px) {
		section.services div.services-text {
			gap: var(--spacing-xl);
		}
	}
</style>
