<script lang="ts">
	import RecentProjects from "$lib/components/RecentProjects.svelte";
	import SeoHead from "$lib/components/SeoHead.svelte";
	import PrimaryButton from "$lib/components/PrimaryButton.svelte";
</script>

<SeoHead
	title="Contact | Kootenay Deluxe"
	description="Contact our team to discuss your construction or electrical project in Rossland and the West Kootenays. Request a quote or ask us how we can help."
/>

<main>
	<section class="contact">
		<div class="contact-text-links">
			<div class="contact-text">
				<h1 class="heading-small">Contact Us</h1>
				<h2 class="heading-large">We'd love to hear from you</h2>
				<p class="body-regular">If you have any questions or would like to request a quote, please reach out.</p>
			</div>
			<div class="contact-links">
				<p class="icon-heading body-regular"><span class="material-icons">location_on</span>Rossland, British Columbia</p>
				<a href="tel:+12505052754" class="icon-heading body-regular"><span class="material-icons">phone</span>+1 (250) 505-2754</a>
				<a href="mailto:chris@kootenaydeluxe.com" class="icon-heading body-regular"
					><span class="material-icons">email</span>chris@kootenaydeluxe.com</a
				>
			</div>
		</div>
		<form>
			<label class="heading-small">
				<span> First Name:</span>
				<input type="text" name="firstName" placeholder="Enter first name" required />
			</label>
			<label class="heading-small">
				<span> Last Name:</span>
				<input type="text" name="lastName" placeholder="Enter last name" required />
			</label>
			<label class="heading-small">
				<span> Email:</span>
				<input type="email" name="email" placeholder="Enter email" required />
			</label>
			<label class="heading-small">
				<span> Phone Number:</span>
				<input type="tel" name="phone" placeholder="Enter phone number" required />
			</label>
			<label class="heading-small text-area">
				<span> Message:</span>
				<textarea name="message" placeholder="Enter your message" required></textarea>
			</label>
			<PrimaryButton type="submit" text="Send Message" />
		</form>
	</section>
	<RecentProjects />
</main>

<style>
	section.contact {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-l);
	}

	section.contact div.contact-text-links {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-l);
	}

	section.contact div.contact-text {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-xs);
		height: fit-content;
	}

	section.contact div.contact-text h1 {
		color: var(--color-primary);
	}

	section.contact div.contact-links {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-s);
		height: fit-content;
	}

	section.contact div.contact-links > * {
		letter-spacing: unset;
	}

	section.contact form {
		display: grid;
		grid-template-columns: 1fr;
		gap: var(--spacing-m);
	}

	section.contact form label {
		position: relative;
		display: flex;
		flex-direction: column;
		gap: var(--spacing-s);
	}

	section.contact form label span {
		font-family: var(--font-heading);
		letter-spacing: 0.1em;
	}
	section.contact form label span::after {
		content: "*";
		color: var(--color-primary);
	}

	section.contact form label textarea {
		min-height: 150px;
		resize: none;
	}

	section.contact form label input,
	section.contact form label textarea {
		padding: var(--spacing-s);
		border: 3px solid var(--color-white);
		font-family: var(--font-body);
		font-size: var(--font-body-m);
		background-color: transparent;
	}

	section.contact form label input:focus-visible,
	section.contact form label textarea:focus-visible {
		outline: none;
		border: 3px solid var(--color-primary);
	}

	@media (min-width: 768px) {
		section.contact form {
			grid-template-columns: repeat(2, 1fr);
		}

		section.contact form label.text-area {
			grid-column: 1 / -1;
		}
	}

	@media (min-width: 1024px) {
		section.contact {
			grid-template-columns: 1fr 1fr;
		}

		section.contact div.contact-text-links {
			justify-content: space-between;
		}
	}
</style>
