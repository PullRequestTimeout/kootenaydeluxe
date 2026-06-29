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
	<a {href} class={primary ? "primary" : "secondary"}>{text} </a>
{:else}
	<button class={primary ? "primary" : "secondary"} onclick={onAction} {type}>{text} </button>
{/if}

<style>
	a,
	button {
		border: none;
		overflow: hidden;
		display: block;
		position: relative;
		padding: 0.7em 2.4em;
		font-size: var(--font-body-m);
		background: transparent;
		cursor: pointer;
		user-select: none;
		color: var(--color-primary);
		z-index: 1;
		font-weight: 500;
		width: fit-content;
		min-width: fit-content;
		font-family: "Bebas Neue", sans-serif;
		letter-spacing: 0.1em;
		font-size: var(--font-body-m);
		transition: color 0.3s;
		border: 4px solid var(--color-primary);
	}

	a::before,
	button::before {
		content: "";
		position: absolute;
		inset: 0;
		background: var(--color-primary);
		transform: scaleX(0);
		transform-origin: right;
		transition: transform 0.3s ease-in-out;
		z-index: -1;
	}

	a:hover,
	button:hover {
		color: var(--color-background-dark-grey);
	}

	a:hover::before,
	button:hover::before {
		transform: scaleX(1);
		transform-origin: left;
	}

	a.secondary,
	button.secondary {
		color: var(--color-background-dark-grey);
		background: var(--color-primary);
	}

	a:hover.secondary,
	button:hover.secondary {
		color: var(--color-primary);
	}

	a.secondary::before,
	button.secondary::before {
		background: var(--color-background-dark-grey);
	}
</style>
