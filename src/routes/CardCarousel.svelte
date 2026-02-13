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
		class="flex flex-row max-w-3/4 items-center gap-3 grow-1 pt-[32px] pb-[128px] overflow-hidden"
	>
		<div
			class={cn(
				'pointer-events-auto',
				'flex flex-col overflow-hidden',
				'w-fit max-h-full',
				'overflow-scroll',
				'p-5 rounded-3xl',
				'bg-(--white-main) shadow-[2px_8px_0px_var(--transp-shad)]'
			)}
		>
			<img
				class="rounded-xl font-black size-full object-contain mb-3"
				src={currentCard?.img}
				alt={currentCard?.imgAlt}
			/>
			<h2 class="text-2xl mt-2 w-full text-center">
				{currentCard?.label}
			</h2>
			<p class="text-xl mt-2 w-full text-center">
				{currentCard?.des}
			</p>
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
		<div
			class="flex flex-row items-center justify-center rounded-full w-[120px] min-h-[65px] px-6 text-(--white-main) bg-(--main-dark)"
			style={`
				box-shadow:
				inset 0px 0px 0px 5px var(--main-dark-shad),
				0px 2px 0px var(--main-dark-shad),
				0px 4px 0px var(--main-dark-shad),
				0px 6px 0px var(--main-dark-shad),
				0px 8px 0px var(--main-dark-shad),
				0px 10px 0px var(--main-dark-shad),
				2px 17px 0px var(--transp-shad);
			`}
		>
			<span class="text-2xl">
				{currentCardIndex + 1} / {cards.length}
			</span>
		</div>

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
