<script lang="ts">
	import FAQ from "$lib/components/FAQ.svelte";
	import { homeFaqs } from "$lib/data/faqs.js";
	import SeoHead from "$lib/components/SeoHead.svelte";
</script>

<SeoHead
	title="About Us | Kootenay Deluxe"
	description="Serving Rossland and the West Kootenays with construction and electrical services built on quality workmanship and practical expertise."
/>

<svelte:head>
	<style>
		section.hero div.hero-image,
		section.hero img {
			width: 100%;
		}

		section.hero ul.hero-list {
			display: grid;
			grid-template-columns: 1fr;
			gap: var(--spacing-m);
			width: 100%;
			padding: 0;
		}

		section.hero ul.hero-list li.hero-list-item {
			list-style: none;
			display: flex;
			flex-direction: column;
			gap: var(--spacing-xs);
		}

		section.hero ul.hero-list div.icon-heading {
			margin: 0;
		}

		section.hero ul.hero-list li p {
			text-align: left;
		}

		@media (min-width: 768px) {
			section.hero ul.hero-list {
				grid-template-columns: 1fr 1fr;
				gap: var(--spacing-l);
			}

			section.hero div.hero-image,
			section.hero ul.hero-list {
				margin-top: var(--spacing-l);
			}
		}
	</style>
</svelte:head>

<main>
	<section class="hero">
		<h1>About Us</h1>
		<h2 class="heading-large">Building With Integrity since 2015</h2>
		<p class="body-regular">
			Serving Rossland and the West Kootenays with construction and electrical services built on quality workmanship and practical expertise.
		</p>
		<div class="hero-image">
			<img src="/assets/images/carousel/3.jpg" alt="Kootenay deluxe van" />
		</div>
		<ul class="hero-list">
			<li class="hero-list-item">
				<div class="icon-heading">
					<span class="material-icons">verified</span>
					<p class="heading-small">Quality Workmanship</p>
				</div>
				<p class="body-regular">
					Every project is completed with care, precision, and attention to detail. We take pride in delivering work that not only looks great on day
					one but continues to perform for years to come.
				</p>
			</li>
			<li class="hero-list-item">
				<div class="icon-heading">
					<span class="material-icons">shield</span>
					<p class="heading-small">Warranty-Backed Work</p>
				</div>
				<p class="body-regular">
					Confidence comes from standing behind what we build. Our work is backed by warranty, giving you added peace of mind long after the project
					is complete.
				</p>
			</li>
			<li class="hero-list-item">
				<div class="icon-heading">
					<span class="material-icons">receipt_long</span>
					<p class="heading-small">Transparent Pricing</p>
				</div>
				<p class="body-regular">
					Clear expectations start with clear pricing. We provide honest estimates and straightforward communication so you can make informed
					decisions without worrying about unexpected costs.
				</p>
			</li>
			<li class="hero-list-item">
				<div class="icon-heading">
					<span class="material-icons">handshake</span>
					<p class="heading-small">Start-to-Finish Reliability</p>
				</div>
				<p class="body-regular">
					From the initial consultation to the final walkthrough, we're committed to showing up, following through, and keeping your project moving
					forward with professionalism and accountability.
				</p>
			</li>
		</ul>
	</section>
	<section class="team">
		<div class="team-text">
			<h2 class="heading-small">Meet the Team</h2>
			<h3 class="heading-large">The People Behind Every Project</h3>
			<p class="body-regular">
				Every member of our team shares the same commitment to craftsmanship, safety, and professionalism. Together, we work to ensure every project
				is completed to a high standard and built to last.
			</p>
		</div>
		<div class="team-members">
			<div class="team-member">
				<div class="team-member-image">
					<img src="/assets/images/team/1.jpg" alt="Kootenay Deluxe team member" />
				</div>
				<h4 class="heading-small">Chris Deluce — Owner</h4>
				<p class="body-regular">
					Electrician and contractor, Chris has built a reputation in Rossland over the years for providing an exceptional standard of work.
				</p>
			</div>
			<div class="team-member">
				<div class="team-member-image">
					<img src="/assets/images/team/2.jpg" alt="Kootenay Deluxe team member" />
				</div>
				<h4 class="heading-small">Allen(?) — Project Manager</h4>
				<p class="body-regular">
					Allen has been with Kootenay Deluxe since [year] and has a wealth of experience in construction and project management. He ensures that
					every project runs smoothly and meets our high standards.
				</p>
			</div>
			<div class="team-member">
				<div class="team-member-image">
					<img src="/assets/images/team/3.jpg" alt="Kootenay Deluxe team member" />
				</div>
				<h4 class="heading-small">Joseph Peters — Carpenter</h4>
				<p class="body-regular">
					Joseph is a skilled carpenter with a passion for creating beautiful and functional spaces. His attention to detail and craftsmanship is
					evident in every project he works on.
				</p>
			</div>
			<div class="team-member">
				<div class="team-member-image">
					<img src="/assets/images/team/4.jpg" alt="Kootenay Deluxe team member" />
				</div>
				<h4 class="heading-small">Another Employee — Position</h4>
				<p class="body-regular">Description of the employee's role and contributions to the team.</p>
			</div>
		</div>
	</section>
	<FAQ faqs={homeFaqs} />
</main>

<style>
	/* Team */
	section.team {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-l);
	}

	section.team div.team-text {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-s);
	}

	section.team div.team-text h2 {
		color: var(--color-primary);
	}

	section.team div.team-members {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-m);
	}

	section.team div.team-members div.team-member {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-xs);
	}

	section.team div.team-members div.team-member div.team-member-image {
		width: 100%;
		aspect-ratio: 1/1;
		overflow: hidden;
		background-color: #f0f0f0;
		margin-bottom: var(--spacing-m);
	}

	section.team div.team-members div.team-member div.team-member-image img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	@media (min-width: 768px) {
		section.team div.team-members {
			grid-template-columns: 1fr 1fr;
			gap: var(--spacing-l);
		}
	}
	@media (min-width: 1024px) {
		section.team {
			grid-template-columns: 1fr 2fr;
			gap: var(--spacing-xl);
		}
	}
</style>
