<script lang="ts">
	import { cn } from '$lib/utils';
	import IconButton from './IconButton.svelte';

	let { currentCardIndex = $bindable(0), cards = [] } = $props();

	// let currentCardIndex = $state(0);
	let currentCard = $derived(cards[currentCardIndex]);

	function previousCard() {
		currentCardIndex = Math.max(0, currentCardIndex - 1);
	}

	function nextCard() {
		currentCardIndex = Math.min(cards.length - 1, currentCardIndex + 1);
	}

	console.log(cards);
</script>

<div class="flex flex-col items-center h-full pointer-events-none">
	<div
		class="flex flex-row max-w-[800px] items-center gap-3 grow-1 pt-[32px] pb-[128px] overflow-hidden"
	>
		<div
			class={cn(
				'pointer-events-auto',
				'flex flex-col overflow-hidden',
				'max-h-full', 
				'overflow-scroll',
				'm-6 p-5 rounded-3xl',
				'bg-(--white-main) shadow-[2px_8px_0px_var(--transp-shad)]'
			)}
		>
			{#if currentCard?.trailer}
				<iframe 
					width="560" 
					height="315" 
					src={currentCard.trailer} 
					title="YouTube video player" 
					frameborder="0" 
					allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
					referrerpolicy="strict-origin-when-cross-origin" 
					allowfullscreen>
				</iframe>
			{:else if currentCard?.carouselImg}
				<img
					class="rounded-xl font-black size-full min-h-[400px] object-contain mb-3"
					src={currentCard?.carouselImg}
					alt={currentCard?.carouselImgAlt}
				/>
			{:else}
				<img
					class="rounded-xl font-black size-full min-h-[400px] object-contain mb-3"
					src={currentCard?.img}
					alt={currentCard?.imgAlt}
				/>
			{/if}
			<div>
				<p class="text-md mt-2 w-full text-center text-(--white-text)">
					{currentCardIndex + 1} / {cards.length}
				</p>
				<div class="flex flex-row mt-1 gap-3 items-center justify-center">
					{#if currentCard?.starred}
						<img src="src/lib/assets/icons/star_outlined.png" alt="star" class="star w-8"/>
					{/if}
					<h2 class="text-2xl text-center">
						{currentCard?.label}
					</h2>
				</div>
				{#if currentCard?.description}
					<p class="text-xl mt-2 w-full text-center">
						{@html currentCard?.description}
					</p>
				{/if}
				{#if currentCard?.longDescription}
					<p class="text-lg mt-2 w-full text-left">
						{@html currentCard?.longDescription}
					</p>
				{/if}
			</div>
		</div>
	</div>

	<div
		class="pointer-events-auto absolute bottom-0 flex flex-row items-center justify-center gap-3 grow-0 p-8"
	>
		<IconButton
			icon="/src/lib/assets/icons/arrow_left.svg"
			alt="email"
			--mainColor="var(--main-dark)"
			--secColor="var(--main-dark-shad)"
			--shadColor="var(--main-dark-shad)"
			onclick={() => {
				previousCard();
			}}
		/>
		<IconButton
			icon="/src/lib/assets/icons/arrow_right.svg"
			alt="email"
			--mainColor="var(--main-dark)"
			--secColor="var(--main-dark-shad)"
			--shadColor="var(--main-dark-shad)"
			--textColor="var(--main-dark-text)"
			onclick={() => {
				nextCard();
			}}
		/>
	</div>
</div> 


<style>
	.star {
		animation: constantRotation 8s linear infinite;
	}

	@keyframes constantRotation {
		0% {
			transform: rotate(0);
		}
		100% {
			transform: rotate(360deg);
		}
	}
</style>