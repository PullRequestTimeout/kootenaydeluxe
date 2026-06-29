<script lang="ts">
	import "material-icons/iconfont/filled.css";

	let { children } = $props();

	import FinalCTA from "$lib/components/FinalCTA.svelte";
	import Footer from "$lib/components/Footer.svelte";
	import Nav from "$lib/components/Nav.svelte";
</script>

<Nav />
{@render children()}
<FinalCTA />
<Footer />

<style>
</style>
