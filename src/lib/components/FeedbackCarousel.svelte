<script lang="ts">
	import emblaCarouselSvelte from "embla-carousel-svelte";
	import Autoplay from "embla-carousel-autoplay";

	let emblaApi: any;
	let options = { loop: true };
	let selectedIndex = $state(0);
	let slideCount = $state(0);

	function onInit(event: any) {
		emblaApi = event.detail;
		slideCount = emblaApi.slideNodes().length;
		selectedIndex = emblaApi.selectedScrollSnap();
		emblaApi.on("select", updateSelectedIndex);
	}

	function updateSelectedIndex() {
		selectedIndex = emblaApi.selectedScrollSnap();
	}

	let plugins = [Autoplay({ delay: 10000 })];

	const feedback = [
		{
			quote:
				"Really solid experience from start to finish. Communication was clear, they showed up when they said they would, and the work was done quickly without cutting corners. Everything was left clean and working perfectly — would definitely use them again.",
			client: "— Mark R."
		},
		{
			quote:
				"From the initial quote to the final walkthrough, the entire process was smooth and professional. The team communicated clearly, stayed on schedule, and the quality of the finished work exceeded our expectations. We'd happily work with them again.",
			client: "— John D."
		},
		{
			quote:
				"We hired them for both construction and electrical work during our renovation, and everything was completed to a high standard. They were reliable, easy to work with, and always took the time to answer our questions along the way.",
			client: "— Sarah L."
		}
	];

	function scrollPrev() {
		emblaApi && emblaApi.scrollPrev();
	}
	function scrollNext() {
		emblaApi && emblaApi.scrollNext();
	}
	function scrollTo(index: number) {
		emblaApi && emblaApi.scrollTo(index);
	}
</script>

<section class="feedback-carousel">
	<div class="feedback-carousel-text">
		<h2 class="heading-large">What Our Clients Say</h2>
		<p class="body-regular">We're proud to earn the trust of our clients through quality work and dependable service.</p>
	</div>
	<div class="embla" use:emblaCarouselSvelte={{ options, plugins }} onemblaInit={onInit}>
		<div class="embla__container">
			{#each feedback as feedbackItem, index}
				<div class="embla__slide">
					<span class="material-icons">format_quote</span>
					<div>
						<p>{feedbackItem.quote}</p>
						<p>{feedbackItem.client}</p>
					</div>
					<span class="material-icons">format_quote</span>
				</div>
			{/each}
		</div>
		<div class="embla__buttons">
			<button onclick={scrollPrev} aria-label="Previous slide"><span class="material-icons">arrow_back_ios</span></button>
			<div class="embla__dots">
				{#each Array(feedback.length) as _, i}
					<button
						class:selected={selectedIndex === i}
						onclick={() => scrollTo(i)}
						aria-label={`Go to slide ${i + 1}`}
						aria-current={selectedIndex === i}
					></button>
				{/each}
			</div>
			<button onclick={scrollNext} aria-label="Next slide"><span class="material-icons">arrow_forward_ios</span></button>
		</div>
	</div>
</section>

<style>
	section.feedback-carousel {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: var(--spacing-l);
	}

	div.feedback-carousel-text {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
	}

	div.feedback-carousel-text h2 {
		max-width: 1200px;
	}

	div.feedback-carousel-text p {
		max-width: 600px;
	}

	div.embla {
		width: 100%;
		position: relative;
		overflow: hidden;
	}

	div.embla__container {
		display: flex;
		align-items: center;
	}

	div.embla__slide {
		min-width: 100%;
		height: 100%;
		font-size: var(--font-body-s);
		color: var(--color-white);
		text-align: center;
		display: flex;
		justify-content: center;
		gap: var(--spacing-xs);
	}

	div.embla__slide span {
		font-size: 2rem;
		color: var(--color-primary);
		opacity: 0.75;
		margin: 0;
	}

	div.embla__slide span:first-child {
		transform: scaleX(-1);
	}

	div.embla__slide span:last-child {
		place-self: end;
	}

	div.embla__slide p {
		max-width: 600px;
		line-height: 1.4;
		font-weight: 400;
		font-size: var(--font-body-m);
		margin: 0;
	}

	div.embla__slide > div {
		display: grid;
		grid-template-columns: 1fr;
	}

	div.embla__slide > div p:last-child {
		font-weight: 700;
		margin-top: var(--spacing-s);
	}

	div.embla__buttons {
		position: relative;
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 1rem;
		margin-top: 1rem;
	}

	div.embla__buttons button {
		background: transparent;
		border: none;
		border-radius: 50%;
		width: 2.5rem;
		height: 2.5rem;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 1.5rem;
		cursor: pointer;
	}

	@media (hover: hover) {
		div.embla__buttons button {
			opacity: 0.5;
			transition: 0.2s;
		}

		div.embla__buttons button:hover {
			opacity: 1;
		}
	}

	div.embla__buttons button span {
		color: var(--color-primary);
		font-size: 2rem;
	}

	div.embla__dots {
		display: flex;
		gap: 1.5rem;
	}

	div.embla__dots button {
		background: var(--color-primary);
		width: 0.75rem;
		height: 0.75rem;
		border-radius: 50%;
		padding: 0;
		opacity: 0.5;
	}

	div.embla__dots button.selected,
	div.embla__dots button[aria-current="true"] {
		opacity: 1;
	}

	@media screen and (min-width: 1024px) {
		section.feedback-carousel {
			gap: var(--spacing-xl);
		}
	}
</style>
