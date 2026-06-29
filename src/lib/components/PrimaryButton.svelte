<script lang="ts">
	// Type definition for the component's props
	type PrimaryButtonProps = {
		href?: string;
		text?: string;
		primary?: boolean;
		type?: "button" | "submit" | "reset";
		onAction?: (event: MouseEvent) => void;
	};

	// Destructure props with default values
	let { href, text = "Button", primary = true, type = "button", onAction }: PrimaryButtonProps = $props();
</script>

{#if href}
	<a {href} class={primary ? "primary" : "secondary"}
		>{text}
		<span></span>
	</a>
{:else}
	<button class={primary ? "primary" : "secondary"} onclick={onAction} {type}
		>{text}
		<span></span>
	</button>
{/if}

<style>
	a,
	button {
		border: none;
		display: block;
		position: relative;
		padding: 0.7em 2.4em;
		font-size: 18px;
		background: transparent;
		cursor: pointer;
		user-select: none;
		overflow: hidden;
		color: var(--color-primary);
		z-index: 1;
		font-family: inherit;
		font-weight: 500;
		width: fit-content;
		min-width: fit-content;
		font-family: "Bebas Neue", sans-serif;
		letter-spacing: 0.1em;
		font-size: var(--font-body-m);
	}

	a span,
	button span {
		position: absolute;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
		background: transparent;
		z-index: -1;
		border: 4px solid var(--color-primary);
	}

	a span::before,
	button span::before {
		content: "";
		display: block;
		position: absolute;
		width: 8%;
		height: 500%;
		background: var(--color-background-dark-grey);
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%) rotate(-60deg);
		transition: all 0.3s;
	}

	a:hover span::before,
	button:hover span::before {
		transform: translate(-50%, -50%) rotate(-90deg);
		width: 100%;
		background: var(--color-primary);
	}

	a:hover,
	button:hover {
		color: var(--color-white);
	}

	a:active span::before,
	button:active span::before {
		background: var(--color-primary);
	}

	/* a,
	button {
		position: relative;
		display: inline-block;
		padding: 0.35rem 1.5rem 0.5rem 1.5rem;
		border-radius: var(--border-radius);
		text-decoration: none;
		font-size: 16px;
		font-weight: 600;
		background-color: var(--color-primary);
		overflow: hidden;
		color: var(--color-white);
		transition: 0.25s ease-out;
		width: fit-content;
	}

	button {
		border: 0;
		cursor: pointer;
	}

	a span,
	button span {
		position: relative;
		z-index: 1;
		text-transform: capitalize;
	}

	a > div,
	button > div {
		position: absolute;
		top: var(--top);
		left: var(--left);
		transform: translate(-50%, -50%);
		width: 0;
		height: 0;
		border-radius: 50%;
		pointer-events: none;
		touch-action: none;
		background-color: var(--color-primary-light);
		transition:
			width 0.4s ease-out,
			height 0.4s ease-out;
	}

	a.secondary,
	button.secondary {
		background-color: transparent;
		border: none;
		padding: calc(0.35rem + var(--border-width)) calc(1.5rem + var(--border-width)) calc(0.5rem + var(--border-width))
			calc(1.5rem + var(--border-width));
		box-shadow: inset 0 0 0 var(--border-width) var(--color-primary);
		color: var(--color-primary);
		transition: color 0.4s ease-out;
	}

	a.secondary > div,
	button.secondary > div {
		background-color: var(--color-primary);
	}

	@media (hover: hover) {
		a:hover > div,
		button:hover > div {
			width: 30rem;
			height: 30rem;
		}

		a.secondary:hover,
		button.secondary:hover {
			color: var(--color-white);
		}
	} */
</style>
