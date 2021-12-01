<script context="module" lang="ts">
	export const prerender = true;
	let notes = [
		{
			id: 1,
			title: 'Svelte',
			category: 'JS',
			content: 'This is the content of this note, asd asd asd asd asd asdasda sdasd '
		},
		{
			id: 2,
			title: 'Tailwind',
			category: 'CSS',
			content: 'This could be an intro to svelt,so you need to keep calm and see the magic'
		},
		{
			id: 3,
			title: 'firestore',
			category: 'Database',
			content: 'This could be an intro to svelt,so you need to keep calm and see the magic'
		}
	];
	const silClick = (id) => {
		console.log(id);
		notes = notes.filter((note) => note.id !== id);
	};
</script>

<script lang="ts">
	import Counter from '$lib/Counter.svelte';
</script>

<svelte:head>
	<title>Svelte - Tailwind - Firebase</title>
</svelte:head>

<section>
	{#each notes as note}
		<div class="max-w-sm rounded overflow-hidden shadow-lg">
			<div class="px-6 pt-4 pb-2 font-bold">{note.title} - {note.category}</div>
			<div class="px-6 py-4">
				<p class="text-gray-700 text-base inline-block">{note.content}</p>

				<button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
					>🔨</button
				>
				<button
					class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded"
					on:click={() => silClick(note.id)}>🧨</button
				>
			</div>
		</div>
	{/each}
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>
