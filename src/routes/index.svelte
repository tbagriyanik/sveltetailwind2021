<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Counter from '$lib/Counter.svelte';
</script>

<svelte:head>
	<title>Svelte - Tailwind - Firebase</title>
</svelte:head>

<section>
	<h2>Svelte - Tailwind ve Firestore Uygulaması</h2>
	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>
