<script lang="ts">
	import FeedbackCarousel from "$lib/components/FeedbackCarousel.svelte";
</script>

<main>
	<section class="hero">
		<h1 class="heading-small">Our Work</h1>
		<h2 class="heading-large">See Our Recent Projects</h2>
		<p class="body-regular">A selection of recent electrical and contracting work completed for homeowners in the Kootenays.</p>
	</section>
	<section class="portfolio">
		<div class="portfolio-item" id="project1">
			<div class="portfolio-item-text">
				<div class="portfolio-item-text-heading">
					<h3 class="heading-large">Kitchen Sunroom Addition</h3>
					<p class="body-regular">
						Expanded the home's living space with a bright, functional sunroom designed to connect seamlessly with the existing kitchen.
					</p>
				</div>
				<div class="portfolio-item-text-details">
					<div class="portfolio-item-text-detail">
						<h4 class="heading-small">Client</h4>
						<p class="body-regular">Homeowner</p>
					</div>
					<div class="portfolio-item-text-detail">
						<h4 class="heading-small">Location</h4>
						<p class="body-regular">Rossland</p>
					</div>
					<div class="portfolio-item-text-detail">
						<h4 class="heading-small">Services</h4>
						<p class="body-regular">House Expansion</p>
					</div>
					<div class="portfolio-item-text-detail">
						<h4 class="heading-small">Completed</h4>
						<p class="body-regular">Jan 2026</p>
					</div>
				</div>
			</div>
			<div class="portfolio-item-image">
				<img src="/assets/images/projects/project1.jpg" alt="Kitchen Sunroom Addition" />
			</div>
		</div>
		<div class="portfolio-item" id="project2">
			<div class="portfolio-item-text">
				<div class="portfolio-item-text-heading">
					<h3 class="heading-large">Exterior Siding Upgrade</h3>
					<p class="body-regular">
						Refreshed the home's exterior with durable new siding, improving both curb appeal and long-term weather protection.
					</p>
				</div>
				<div class="portfolio-item-text-details">
					<div class="portfolio-item-text-detail">
						<h4 class="heading-small">Client</h4>
						<p class="body-regular">Homeowner</p>
					</div>
					<div class="portfolio-item-text-detail">
						<h4 class="heading-small">Location</h4>
						<p class="body-regular">Rossland</p>
					</div>
					<div class="portfolio-item-text-detail">
						<h4 class="heading-small">Services</h4>
						<p class="body-regular">House Expansion</p>
					</div>
					<div class="portfolio-item-text-detail">
						<h4 class="heading-small">Completed</h4>
						<p class="body-regular">Jan 2026</p>
					</div>
				</div>
			</div>
			<div class="portfolio-item-image">
				<img src="/assets/images/projects/project2.jpg" alt="Exterior Siding Upgrade" />
			</div>
		</div>
	</section>
	<FeedbackCarousel />
</main>

<style>
	/* Portfolio */
	section.portfolio {
		display: grid;
		gap: var(--spacing-l);
	}

	section.portfolio div.portfolio-item {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-m);
	}

	section.portfolio div.portfolio-item div.portfolio-item-text {
		display: grid;
		gap: var(--spacing-m);
	}

	section.portfolio div.portfolio-item div.portfolio-item-text div.portfolio-item-text-details {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: var(--spacing-s);
	}

	section.portfolio div.portfolio-item div.portfolio-item-image {
		width: 100%;
		max-height: calc(var(--vh, 1vh) * 85);
	}

	section.portfolio div.portfolio-item div.portfolio-item-image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	@media (min-width: 640px) {
		section.portfolio div.portfolio-item,
		section.portfolio div.portfolio-item div.portfolio-item-text {
			gap: var(--spacing-l);
		}
	}

	@media (min-width: 1024px) {
		section.portfolio {
			gap: var(--spacing-xl);
		}

		section.portfolio div.portfolio-item div.portfolio-item-text {
			grid-template-columns: 1.5fr 1fr;
		}
	}
</style>
