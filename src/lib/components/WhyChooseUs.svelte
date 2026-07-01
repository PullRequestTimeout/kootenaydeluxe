<section class="why-us">
	<div class="why-us-text">
		<h2 class="heading-small">Why Choose Us?</h2>
		<h3 class="heading-large">Built on Quality, Safety & Trust</h3>
		<p class="body-regular">We approach every project with attention to detail, strict safety standards, and a commitment to doing the job right.</p>
	</div>
	<div class="why-us-list">
		<div class="why-us-item">
			<div class="icon-heading">
				<span class="material-icons">check_circle</span>
				<p class="heading-small">Quality Workmanship</p>
			</div>
			<p class="body-regular">Careful attention to detail and a commitment to doing the job properly.</p>
		</div>
		<div class="why-us-item">
			<div class="icon-heading">
				<span class="material-icons">check_circle</span>
				<p class="heading-small">Warranty-Backed Work</p>
			</div>
			<p class="body-regular">Every project is supported by a workmanship guarantee, offering long-term confidence in the result.</p>
		</div>
		<div class="why-us-item">
			<div class="icon-heading">
				<span class="material-icons">check_circle</span>
				<p class="heading-small">Transparent Pricing</p>
			</div>
			<p class="body-regular">Clear, upfront estimates with no hidden costs, so expectations are set from the very beginning.</p>
		</div>
		<div class="why-us-item">
			<div class="icon-heading">
				<span class="material-icons">check_circle</span>
				<p class="heading-small">Start-to-Finish Reliability</p>
			</div>
			<p class="body-regular">Consistent communication, dependable scheduling, and a job that gets done right the first time.</p>
		</div>
	</div>
	<a href="/contact" class="body-regular">Get a Free Quote <span class="material-icons">arrow_outward</span></a>
</section>

<style>
	/* Why Us */
	section.why-us {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-l);
	}
	section.why-us div.why-us-text,
	section.why-us div.why-us-item {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-xs);
	}

	section.why-us div.why-us-text {
		align-items: center;
		text-align: center;
	}

	section.why-us div.why-us-text h2 {
		color: var(--color-primary);
	}

	section.why-us div.why-us-text h3 {
		max-width: 1200px;
	}

	section.why-us div.why-us-text p {
		max-width: 600px;
	}

	section.why-us div.why-us-list {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-m);
	}

	section.why-us a {
		text-decoration: underline;
		font-weight: 400;
		text-align: center;
	}

	section.why-us a span {
		color: var(--color-white);
		transform: translateY(0.25em);
	}

	@media (min-width: 640px) {
		section.why-us div.why-us-list {
			grid-template-columns: 1fr 1fr;
			gap: var(--spacing-l);
		}
	}

	@media (min-width: 1024px) {
		section.why-us div.why-us-list {
			grid-template-columns: repeat(4, 1fr);
			gap: var(--spacing-l);
		}
	}

	@media (min-width: 1280px) {
		section.why-us {
			gap: var(--spacing-xl);
		}
	}
</style>
