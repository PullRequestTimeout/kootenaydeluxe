<script lang="ts">
	import PrimaryButton from "$lib/components/PrimaryButton.svelte";
</script>

<main>
	<section class="hero">
		<h1>Kootenay Deluxe</h1>
		<h2 class="heading-large">Reliable Contracting & Electrical Services in Rossland, British Columbia</h2>
		<p class="body-regular">From small repairs to full-scale projects, we deliver safe, efficient, and code-compliant work you can count on.</p>
		<div>
			<PrimaryButton text="Get a Quote" href="/contact" primary={false} />
			<PrimaryButton text="Call Now" href="/contact" primary />
		</div>
	</section>
</main>

<style>
</style>
