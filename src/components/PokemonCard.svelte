<script lang="ts">
	import type { BasePokemon } from 'src/stores/pokemon';

	import { fade } from 'svelte/transition';
	export let pokemon: BasePokemon;
</script>

<a
	class="list-none p-6 bg-gray-100 text-gray-800 text-center rounded-md shadow-sm hover:shadow-md flex flex-col items-center"
	href={`/pokemon/${pokemon.id}`}
	transition:fade
>
	<img class="h-40 w-40 " src={pokemon.image} alt={pokemon.name} />
	<h2 class="uppercase text-2xl">{pokemon.id}. {pokemon.name}</h2>
</a>
