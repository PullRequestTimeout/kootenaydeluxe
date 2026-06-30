<script lang="ts">
	import emblaCarouselSvelte from "embla-carousel-svelte";
	import ClassNames from "embla-carousel-class-names";
	import Autoplay from "embla-carousel-autoplay";

	type Slide = {
		image: string;
		alt: string;
	};

	// Add data to lengthen slideshow
	const slides: { [key: string]: Slide } = {
		slide1: {
			image: "1.jpg",
			alt: "Image number 1 of the carousel."
		},
		slide2: {
			image: "2.jpg",
			alt: "Image number 2 of the carousel."
		},
		slide3: {
			image: "3.jpg",
			alt: "Image number 3 of the carousel."
		}
	};

	const options = { loop: true, duration: 60 };
	let plugins = [ClassNames(), Autoplay({ delay: 7000 })];

	let emblaApi: any = $state(null);
	const onInit = (event: any) => {
		emblaApi = event.detail;
	};
</script>

<section class="embla" use:emblaCarouselSvelte={{ options, plugins }} onemblaInit={onInit}>
	<div class="embla__container">
		{#each Object.keys(slides) as slide}
			<div class="embla__slide">
				<img src={`/assets/images/carousel/${slides[slide].image}`} alt={slides[slide].alt} />
			</div>
		{/each}
	</div>
	<button class="embla__prev" onclick={emblaApi.scrollPrev} aria-label="Carousel Previous">
		<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 -960 960 960"><path d="M400-80 0-480l400-400 71 71-329 329 329 329-71 71Z" /></svg></button
	>
	<button class="embla__next" onclick={emblaApi.scrollNext} aria-label="Carousel Next">
		<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 -960 960 960"><path d="m321-80-71-71 329-329-329-329 71-71 400 400L321-80Z" /></svg></button
	>
</section>

<style>
	section.embla {
		/* margin-top: -2px; */
		position: relative;
		overflow: hidden;
		padding: var(--padding-block) var(--padding-inline);
		padding: var(--padding-block) 0;
		background-color: transparent;
	}

	div.embla__container {
		display: flex;
	}

	div.embla__container img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	div.embla__slide {
		flex: 0 0 100%;
		min-width: 0;
		position: relative;
	}

	section.embla > button {
		position: absolute;
		top: 50%;
		cursor: pointer;
		display: flex;
		border: none;
		align-items: center;
		justify-content: center;
		background-color: transparent;
		translate: 0 -50%;
		padding: 0.5rem;
		display: none;
	}

	section.embla > button > svg {
		fill: var(--color-primary);
		width: 2rem;
		height: 2rem;
	}

	button.embla__next {
		right: 1rem;
	}

	button.embla__prev {
		left: 1rem;
	}

	button.embla__prev > svg {
		translate: 0.75rem 0;
	}

	@media screen and (min-width: 768px) {
		section.embla > button {
			display: flex;
		}

		section.embla > button > svg {
			width: 3rem;
			height: 3rem;
			filter: drop-shadow(0 0 0.2rem rgba(0, 0, 0, 0.75));
		}

		div.embla__slide {
			flex: 0 0 80%;
			padding: 0 1rem;
		}
	}

	@media screen and (min-width: 1024px) {
		div.embla__slide {
			flex: 0 0 60%;
			padding: 0 1rem;
		}
	}

	@media (hover: hover) {
		section.embla > button > svg {
			opacity: 0.9;
			transition-duration: 0.1s;
		}

		section.embla > button:hover > svg,
		section.embla > button:active > svg {
			opacity: 1;
			scale: 1.1;
		}
	}
</style>
