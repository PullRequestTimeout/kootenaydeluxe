<script lang="ts">
	function handleCookies() {
		// Implement cookie handling logic here
		alert("Cookie settings will be implemented here.");
	}
</script>

<footer>
	<div class="footer-upper-section">
		<div class="footer-title-contact">
			<div class="footer-title">
				<a href="/">
					<img class="logo" src="/assets/images/kd-logo-white.png" alt="Kootenay Deluxe Logo" />
				</a>
				<p>Reliable Contracting & Electrical Services in Rossland, British Columbia</p>
			</div>
			<div class="footer-contact">
				<a href="mailto:chris@kootenaydeluxe.com"><span class="material-icons">email</span>chris@kootenaydeluxe.com</a>
				<a href="tel:+12505052754"><span class="material-icons">phone</span>+1 (250) 505-2754</a>
			</div>
		</div>
		<div class="footer-links">
			<p class="footer-subtitle">Quick Links</p>
			<div>
				<a href="/">Home</a>
				<a href="/about">About</a>
				<a href="/services">Services</a>
				<a href="/work">Work</a>
				<a href="/contact">Contact</a>
			</div>
		</div>
		<div class="footer-policy-social">
			<div class="footer-policy">
				<p class="footer-subtitle">Policy</p>
				<div>
					<button class="cookies-button" onclick={handleCookies}>Cookies</button>
					<a href="/privacy-policy">Privacy Policy</a>
				</div>
			</div>
			<div class="footer-social">
				<a href="https://www.facebook.com/KootenayDeluxe" target="_blank" rel="noopener noreferrer" aria-label="Facebook">
					<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path
							d="M12.1347 31.5293V20.8893H8.836V16H12.1347V13.8933C12.1347 8.44667 14.5987 5.92267 19.9453 5.92267C20.48 5.92267 21.2187 5.97867 21.9027 6.06C22.415 6.11272 22.9232 6.19958 23.424 6.32V10.7533C23.1345 10.7263 22.8441 10.7103 22.5533 10.7053C22.2276 10.6969 21.9018 10.6929 21.576 10.6933C20.6333 10.6933 19.8973 10.8213 19.3427 11.1053C18.9698 11.2924 18.6563 11.5796 18.4373 11.9347C18.0933 12.4947 17.9387 13.2613 17.9387 14.2707V16H23.164L22.6493 18.804L22.2667 20.8893H17.9387V31.8827C25.8613 30.9253 32 24.18 32 16C32 7.164 24.836 0 16 0C7.164 0 0 7.164 0 16C0 23.504 5.16533 29.8 12.1347 31.5293Z"
							fill="#E2AB60"
						/>
					</svg>
				</a>
				<a href="https://www.instagram.com/kootenaydeluxe/" target="_blank" rel="noopener noreferrer" aria-label="Instagram">
					<svg width="32" height="32" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path
							d="M9.37344 0.112022C7.67104 0.192289 6.50851 0.464023 5.49211 0.863223C4.44037 1.27322 3.54877 1.82322 2.66171 2.71349C1.77478 3.60376 1.22838 4.49589 0.821442 5.54949C0.427575 6.56789 0.160642 7.73149 0.0854421 9.43482C0.0102421 11.1382 -0.00642455 11.6858 0.00197545 16.0308C0.0102421 20.3756 0.0294421 20.9203 0.111975 22.6272C0.193309 24.3292 0.463975 25.4915 0.863309 26.5082C1.27398 27.56 1.82331 28.4512 2.71397 29.3386C3.60451 30.2259 4.49597 30.771 5.55197 31.1786C6.56957 31.5719 7.73344 31.84 9.43651 31.9146C11.1396 31.9892 11.6877 32.0066 16.0314 31.9982C20.3752 31.9899 20.9221 31.9706 22.6285 31.8896C24.3352 31.8087 25.4912 31.536 26.5082 31.1386C27.5601 30.7271 28.452 30.1786 29.3386 29.2878C30.2253 28.3968 30.7713 27.504 31.178 26.4499C31.5722 25.4323 31.8401 24.2686 31.914 22.5667C31.9886 20.8588 32.0062 20.3136 31.998 15.9694C31.9896 11.625 31.97 11.0803 31.889 9.37402C31.8081 7.66776 31.537 6.50909 31.138 5.49176C30.7268 4.43989 30.178 3.54936 29.2878 2.66136C28.3976 1.77336 27.504 1.22776 26.4504 0.822023C25.432 0.428023 24.2689 0.159622 22.5658 0.0860224C20.8628 0.0124224 20.3146 -0.00664428 15.9693 0.00188905C11.624 0.0101557 11.08 0.0288224 9.37344 0.112022ZM9.56037 29.0362C8.00037 28.9683 7.15331 28.7091 6.58877 28.4922C5.84131 28.2042 5.30877 27.856 4.74624 27.2988C4.18357 26.7418 3.83811 26.2074 3.54624 25.4615C3.32704 24.897 3.06304 24.0508 2.99011 22.4908C2.91077 20.8048 2.89411 20.2986 2.88477 16.0268C2.87544 11.7552 2.89184 11.2495 2.96571 9.56282C3.03237 8.00416 3.29317 7.15616 3.50971 6.59189C3.79771 5.84349 4.14464 5.31189 4.70304 4.74976C5.26144 4.18749 5.79424 3.84122 6.54077 3.54936C7.10477 3.32922 7.95077 3.06749 9.51011 2.99322C11.1974 2.91322 11.703 2.89722 15.9741 2.88789C20.2452 2.87856 20.7521 2.89456 22.4401 2.96896C23.9988 3.03669 24.8472 3.29496 25.4108 3.51296C26.1585 3.80096 26.6908 4.14682 27.2529 4.70629C27.8152 5.26549 28.1617 5.79642 28.4536 6.54456C28.674 7.10682 28.9358 7.95256 29.0094 9.51296C29.0897 11.2003 29.108 11.7063 29.1156 15.977C29.1233 20.2476 29.1082 20.7548 29.0342 22.441C28.9662 24.001 28.7076 24.8483 28.4902 25.4135C28.2022 26.1607 27.8552 26.6935 27.2964 27.2554C26.7377 27.8174 26.2056 28.1635 25.4586 28.4554C24.8954 28.6752 24.0484 28.9376 22.4904 29.0119C20.8029 29.0912 20.2973 29.1079 16.0246 29.1172C11.752 29.1266 11.2477 29.1092 9.56037 29.0362ZM22.604 7.44856C22.6046 7.82833 22.7178 8.19939 22.9294 8.51479C23.1409 8.8302 23.4412 9.07579 23.7924 9.2205C24.1435 9.36521 24.5296 9.40254 24.902 9.32778C25.2743 9.25301 25.6161 9.06949 25.8842 8.80045C26.1522 8.53141 26.3344 8.18892 26.4078 7.8163C26.4812 7.44368 26.4424 7.05767 26.2964 6.70709C26.1503 6.35652 25.9036 6.05712 25.5874 5.84677C25.2712 5.63642 24.8997 5.52457 24.52 5.52536C24.0109 5.52642 23.5231 5.72961 23.1638 6.09026C22.8045 6.4509 22.6031 6.93948 22.604 7.44856ZM7.78464 16.016C7.79357 20.5536 11.4788 24.2236 16.0153 24.2151C20.5521 24.2064 24.2246 20.5216 24.2161 15.984C24.2074 11.4464 20.5214 7.77536 15.9841 7.78429C11.4468 7.79322 7.77611 11.479 7.78464 16.016ZM10.6666 16.0103C10.6646 14.9555 10.9753 13.9237 11.5596 13.0455C12.1439 12.1673 12.9755 11.4821 13.9492 11.0765C14.923 10.6709 15.9951 10.5631 17.0301 10.7669C18.065 10.9706 19.0163 11.4767 19.7637 12.221C20.511 12.9654 21.0209 13.9147 21.2287 14.9489C21.4366 15.983 21.3331 17.0556 20.9314 18.0309C20.5297 19.0063 19.8477 19.8406 18.9719 20.4283C18.096 21.0161 17.0655 21.331 16.0106 21.3331C15.3102 21.3346 14.6164 21.198 13.9687 20.9313C13.3211 20.6646 12.7323 20.2729 12.2361 19.7787C11.7398 19.2844 11.3458 18.6972 11.0765 18.0506C10.8072 17.404 10.668 16.7107 10.6666 16.0103Z"
							fill="#E2AB60"
						/>
					</svg>
				</a>
			</div>
		</div>
	</div>
	<hr />
	<div class="footer-lower-section">
		<p>&copy; {new Date().getFullYear()} Kootenay Deluxe Contracting</p>
		<a href="https://www.pixelmountain.ca" target="_blank" rel="noopener noreferrer">
			<img src="/assets/images/pixelmountain-logo.png" alt="Pixel Mountain Logo" />
		</a>
	</div>
</footer>

<style>
	footer {
		background-color: var(--color-black);
		color: var(--color-white);
		padding: var(--padding-block) var(--padding-inline);
	}
	footer * {
		font-size: var(--font-body-m);
	}

	footer,
	footer div {
		display: flex;
		flex-direction: column;
		gap: var(--spacing-s);
	}

	footer a {
		display: flex;
		align-items: center;
		gap: var(--spacing-s);
	}

	footer > div {
		gap: var(--spacing-m);
	}

	footer .footer-subtitle {
		font-weight: bold;
		margin-bottom: var(--spacing-s);
	}

	footer div.footer-title {
		margin-bottom: var(--spacing-m);
	}

	footer div.footer-title img {
		width: 8rem;
	}

	footer hr {
		border: none;
		border-top: var(--border-width) solid var(--color-white);
		margin: var(--spacing-m) 0;
	}

	footer div.footer-links div,
	footer div.footer-policy div {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: var(--spacing-s);
	}

	footer div.footer-policy button {
		border: none;
		background: none;
		color: var(--color-white);
		cursor: pointer;
		font: inherit;
		width: fit-content;
		padding: 0;
		margin: 0;
	}

	footer div.footer-lower-section img {
		width: 12rem;
	}

	footer div.footer-social {
		flex-direction: row;
		gap: var(--spacing-m);
		margin-top: var(--spacing-m);
	}

	@media (hover: hover) {
		footer a,
		footer button {
			transition: color 0.3s ease;
		}

		footer a:hover,
		footer button.cookies-button:hover {
			color: var(--color-primary);
		}
	}

	@media (min-width: 1024px) {
		footer div.footer-title p {
			max-width: 42ch;
			margin-top: var(--spacing-s);
		}

		footer div.footer-title img {
			width: 10rem;
		}

		footer div.footer-upper-section {
			display: grid;
			grid-template-columns: 2fr 1.5fr auto;
			gap: var(--spacing-m);
		}

		footer div.footer-lower-section {
			flex-direction: row;
			justify-content: space-between;
			align-items: center;
		}

		footer div.footer-links div,
		footer div.footer-social,
		footer div.footer-policy div {
			display: grid;
			grid-template-columns: 1fr;
			gap: var(--spacing-s);
		}

		footer div.footer-policy-social {
			justify-content: space-between;
		}

		footer div.footer-social {
			justify-items: end;
			align-items: end;
			text-align: left;
		}
	}
</style>
