<script lang="ts">
	import { cn } from '$lib/utils';
	import Card from './Card.svelte';

	let { cards = [] } = $props();
</script>

<div class="flex w-full justify-center p-6">
	<div class={cn(	
		'flex flex-wrap gap-6 justify-center', 'max-w-[1000px]'
	)}>
		{#each cards as card}
			<Card title={card.label} img={card.img} imgAlt={card.imgAlt}/>
		{/each}
	</div>
</div>