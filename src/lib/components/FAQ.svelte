<script lang="ts">
	import { slide } from "svelte/transition";
	import { isIntersecting } from "$lib/utils/isIntersecting";
	import PrimaryButton from "$lib/components/PrimaryButton.svelte";

	let openFaqIndex: number | null = $state(null);

	function toggleFaq(i: number) {
		openFaqIndex = openFaqIndex === i ? null : i;
	}

	let { faqs = $bindable([]) } = $props();
</script>

<section>
	<div class="faq-text">
		<h2 class="heading-large">Frequently Asked Questions</h2>
		<p class="body-regular">Answers to common questions about our services, pricing, and what to expect when working with us.</p>
		<PrimaryButton text="Ask a Question" href="/contact" primary />
	</div>
	<div class="faq-group group-stagger-fade" use:isIntersecting>
		<hr />
		{#each faqs as faq, i}
			<div class="faq-item">
				<button onclick={() => toggleFaq(i)} aria-label="Toggle answer for {faq.question}">
					<p class="heading-small">{faq.question}</p>
					<div class="faq-icon" class:open={openFaqIndex === i}>
						<span></span>
						<span></span>
					</div>
				</button>
				{#if openFaqIndex === i}
					<div transition:slide={{ axis: "y" }} class="faq-answer">
						{#each faq.answer as answer}
							{#if answer.element === "p"}
								<p>{answer.content}</p>
							{:else if answer.element === "ul"}
								<ul>
									{#if Array.isArray(answer.content)}
										{#each answer.content as item}
											<li>{item}</li>
										{/each}
									{/if}
								</ul>
							{:else if answer.element === "a"}
								{#if typeof answer.content === "object" && answer.content !== null && "href" in answer.content && "text" in answer.content}
									<a href={answer.content.href}>{answer.content.text}</a>
								{/if}
							{/if}
						{/each}
					</div>
				{/if}
			</div>
			<hr />
		{/each}
	</div>
</section>

<style>
	section {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-l);
	}

	div.faq-text {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		gap: var(--spacing-s);
	}

	div.faq-group {
		width: 100%;
	}

	div.faq-item {
		width: 100%;
	}

	div.faq-item button {
		width: 100%;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background: none;
		border: none;
		padding: 0.75rem 0;
		gap: var(--spacing-xs);
	}

	div.faq-item button p {
		text-align: left;
		font-size: var(--font-body-l);
		font-family: "Bebas Neue", sans-serif;
		letter-spacing: 0.05em;
	}

	div.faq-item button * {
		margin: 0;
	}

	div.faq-item div.faq-answer * {
		margin: 0;
		font-size: var(--font-body-m);
		color: var(--color-white);
	}

	div.faq-item div.faq-answer {
		margin-bottom: var(--spacing-m);
		display: flex;
		flex-direction: column;
		gap: var(--spacing-s);
	}

	div.faq-item div.faq-answer a {
		color: var(--color-primary);
		text-decoration: underline;
		font-weight: 400;
	}

	hr {
		width: 100%;
		border: none;
		border-top: 2px solid var(--color-white);
	}

	/* closed */
	div.faq-icon {
		position: relative;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 1rem;
		height: 1rem;
	}

	div.faq-icon span {
		background-color: var(--color-primary);
		height: 0.2rem;
		width: 100%;
		transition: transform 0.3s ease;
		position: absolute;
		top: 50%;
		left: -50%;
		translate:
			-50%,
			-50%;
	}

	div.faq-icon span:first-child {
		transform: rotate(90deg);
	}

	/* open */
	div.faq-icon.open span:first-child {
		transform: rotate(0deg);
	}

	@media screen and (min-width: 1024px) {
		section {
			grid-template-columns: 1.5fr 2fr;
		}

		div.faq-text {
			align-items: flex-start;
			text-align: left;
			gap: var(--spacing-s);
		}
		div.faq-text p {
			margin-bottom: var(--spacing-l);
		}
	}
</style>
