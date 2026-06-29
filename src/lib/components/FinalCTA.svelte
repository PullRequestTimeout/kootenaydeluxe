<script>
	import PrimaryButton from "$lib/components/PrimaryButton.svelte";
</script>

<section>
	<div class="final-cta-content">
		<h2 class="heading-large">Ready to Start Your Next Project?</h2>
		<p class="body-regular">
			Whether you need electrical work, a renovation, or help bringing a larger project to life, we're here to provide reliable service and quality
			workmanship from start to finish.
		</p>
	</div>
	<div class="final-cta-buttons">
		<PrimaryButton text="Get a Quote" href="/contact" primary />
		<PrimaryButton text="Contact Us" href="tel:+1234567890" />
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: var(--spacing-l);
	}

	div.final-cta-buttons,
	div.final-cta-content {
		display: flex;
		gap: var(--spacing-m);
		text-align: center;
	}

	div.final-cta-content {
		flex-direction: column;
	}

	@media (min-width: 1024px) {
		section {
			display: grid;
			grid-template-columns: 2fr 1fr;
			gap: var(--spacing-xl);
		}

		div.final-cta-content {
			text-align: left;
			align-items: flex-start;
		}
	}
</style>
