<script lang="ts">
	import RecentProjects from "$lib/components/RecentProjects.svelte";
	import WhyChooseUs from "$lib/components/WhyChooseUs.svelte";
	import SeoHead from "$lib/components/SeoHead.svelte";
</script>

<SeoHead title="Our Services | Kootenay Deluxe" description="Construction and Electrical Services Throughout the West Kootenays" />

<main>
	<section class="hero">
		<h1>Our Services</h1>
		<h2 class="heading-large">Construction and Electrical Services Throughout the West Kootenays</h2>
		<p class="body-regular">
			Whether you're planning a new build, upgrading an existing property, or tackling a complex electrical project, our team has the experience and
			expertise to help bring it to life.
		</p>
	</section>
	<section class="services">
		<div class="services-item">
			<div class="services-item-text">
				<h2 class="heading-small">Electrical Services</h2>
				<h3 class="heading-large">Safe, Reliable Electrical Solutions for Homes and Businesses</h3>
				<p class="body-regular">
					Professional electrical services for residential and commercial projects, completed safely, efficiently, and to code.
				</p>
				<div class="services-item-projects">
					<h4 class="heading-small">Common Projects:</h4>
					<ul>
						<li class="body-regular">Service and panel upgrades</li>
						<li class="body-regular">New construction wiring</li>
						<li class="body-regular">Lighting installations and upgrades</li>
						<li class="body-regular">Electrical troubleshooting and repairs</li>
						<li class="body-regular">And more!</li>
					</ul>
				</div>
			</div>
			<div class="services-item-image">
				<img src="/images/services/electrical.jpg" alt="Electrical Services" />
			</div>
		</div>
		<div class="services-item">
			<div class="services-item-text">
				<h2 class="heading-small">Construction Services</h2>
				<h3 class="heading-large">Quality Construction Services from Planning to Completion</h3>
				<p class="body-regular">
					Dependable construction services delivered with skilled craftsmanship, attention to detail, and a commitment to quality.
				</p>
				<div class="services-item-projects">
					<h4 class="heading-small">Common Projects:</h4>
					<ul>
						<li class="body-regular">Home renovations and remodels</li>
						<li class="body-regular">Additions and expansions</li>
						<li class="body-regular">Garages, shops, and outbuildings</li>
						<li class="body-regular">Decks and outdoor living spaces</li>
						<li class="body-regular">And more!</li>
					</ul>
				</div>
			</div>
			<div class="services-item-image">
				<img src="/images/services/construction.jpg" alt="Construction Services" />
			</div>
		</div>
	</section>
	<WhyChooseUs />
	<section class="service-area">
		<div class="services-item-text">
			<h2 class="heading-small">Service Area</h2>
			<h3 class="heading-large">Proudly Serving Rossland and Communities Across the West Kootenays</h3>
			<p class="body-regular">
				We've built lasting relationships throughout the region by combining skilled craftsmanship, transparent communication, and dependable service
				on projects of every size.
			</p>
		</div>
		<div class="services-item-image">
			<img src="/assets/images/service-area.jpg" alt="Service Area" />
		</div>
	</section>
	<RecentProjects />
</main>

<style>
	/* Services */
	section.services {
		display: grid;
		gap: var(--spacing-l);
	}

	section.services div.services-item {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-m);
	}

	section.services div.services-item div.services-item-text {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-xs);
	}
	section.services div.services-item div.services-item-text h2 {
		color: var(--color-primary);
	}

	section.services div.services-item div.services-item-text div.services-item-projects {
		margin-top: var(--spacing-s);
	}
	section.services div.services-item div.services-item-text div.services-item-projects h4,
	section.services div.services-item div.services-item-text div.services-item-projects li {
		margin-bottom: var(--spacing-xs);
	}

	section.services div.services-item div.services-item-image {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100%;
		height: 100%;
		min-height: 250px;
		background-color: #f0f0f0;
	}

	section.services div.services-item div.services-item-image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		color: var(--color-black);
	}

	@media (min-width: 640px) {
		section.services div.services-item {
			gap: var(--spacing-l);
		}
	}

	@media (min-width: 1024px) {
		section.services div.services-item {
			grid-template-columns: 1fr 1fr;
			gap: var(--spacing-m) var(--spacing-l);
		}

		section.services div.services-item:nth-child(2) div:first-child {
			grid-column: 2 / 3;
			grid-row: 2 / 3;
		}

		section.services div.services-item:nth-child(2) div:last-child {
			grid-column: 1 / 2;
			grid-row: 2 / 3;
		}

		section.services div.services-item div.services-item-text div.services-item-projects {
			margin-top: max(var(--spacing-m), var(--spacing-s));
		}
	}

	@media (min-width: 1280px) {
		section.services div.services-item {
			gap: var(--spacing-l);
		}
	}

	/* Service Area */
	section.service-area {
		display: grid;
		gap: var(--spacing-l);
	}

	section.service-area div.services-item-text {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-xs);
	}

	section.service-area div.services-item-text h2 {
		color: var(--color-primary);
	}

	section.service-area div.services-item-image {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100%;
		height: 100%;
		min-height: 250px;
		background-color: #f0f0f0;
		overflow: hidden;
	}

	section.service-area div.services-item-image img {
		width: 101%;
		height: 101%;
		object-fit: cover;
		color: var(--color-black);
	}

	@media (min-width: 1024px) {
		section.service-area {
			grid-template-columns: 1fr 1fr;
		}

		section.service-area div.services-item-text {
			align-self: center;
		}
	}
</style>
