<script lang="ts">
	import PrimaryButton from "$lib/components/PrimaryButton.svelte";
</script>

<section class="recent-projects">
	<div class="recent-projects-text">
		<h2 class="heading-small">Recent Projects</h2>
		<h3 class="heading-large">See Our Portfolio</h3>
		<p class="body-regular">A selection of recent electrical and contracting work completed for homeowners in the local area.</p>
	</div>
	<div class="recent-projects-list">
		<div class="recent-projects-item">
			<div class="recent-projects-image"><img src="/assets/images/projects/project1.jpg" alt="Project 1" /></div>
			<h4 class="heading-small">Kitchen Sunroom Addition</h4>
			<p class="body-regular">
				Expanded the home's living space with a bright, functional sunroom designed to connect seamlessly with the existing kitchen.
			</p>
			<a href="/our-work#1">View Project<span class="material-icons">arrow_outward</span></a>
		</div>
		<div class="recent-projects-item">
			<div class="recent-projects-image"><img src="/assets/images/projects/project2.jpg" alt="Project 2" /></div>
			<h4 class="heading-small">Exterior Siding Upgrade</h4>
			<p class="body-regular">Refreshed the home's exterior with durable new siding, improving both curb appeal and long-term weather protection.</p>
			<a href="/our-work#2">View Project<span class="material-icons">arrow_outward</span></a>
		</div>
	</div>
	<PrimaryButton text="View More Projects" href="/our-work" primary />
</section>

<style>
	section.recent-projects {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: var(--spacing-l);
	}

	div.recent-projects-text {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		gap: var(--spacing-xs);
	}

	div.recent-projects-text h2 {
		color: var(--color-primary);
	}

	div.recent-projects-text p {
		max-width: 600px;
	}

	div.recent-projects-list {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-m);
	}

	div.recent-projects-item {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-s);
	}

	div.recent-projects-item img {
		margin-bottom: var(--spacing-m);
	}

	div.recent-projects-item a {
		text-decoration: underline;
	}
	div.recent-projects-item a span {
		color: var(--color-white);
		transform: translateY(0.25em);
	}

	@media (min-width: 1024px) {
		section.recent-projects {
			gap: var(--spacing-xl);
		}

		div.recent-projects-list {
			grid-template-columns: 1fr 1fr;
			gap: var(--spacing-l);
		}
	}
</style>
