<script lang="ts">
	import { cn } from '$lib/utils';

	let { title = '', description = '', img = '', imgAlt = '', starred = false, onclick=(() => {}) } = $props();

	let ref: HTMLElement;

	let initialCardRotation = (Math.random() - 0.5) * 0.1;
	let cardRotation = $state(initialCardRotation);
</script>

<button
	class={cn('w-60 h-70 group')}
	{onclick}
>
	<div
		bind:this={ref}
		class={cn(
			'relative size-full flex flex-col',
			'pointer-events-none',
			'bg-white rounded-2xl p-3',
			'transition-[all,box-shadow_200ms_ease]',
			'ease-(--ease-out-back) duration-300',

			'rotate-[var(--rotation-value)]',
			'shadow-[2px_8px_0px_var(--transp-shad)]',

			'group-hover:-translate-y-2',
			'group-hover:-rotate-2',
			'group-hover:shadow-[3px_16px_0px_var(--transp-shad)]',
		)}
	>
		{#if img}
			<img src={img} alt={imgAlt} class="size-full object-cover rounded-xl" />
		{/if}
		<p class="mt-2 text-xl font-extrabold">
			{title}
		</p>
		{#if description}
			<p class="mt-2 text-md">
				{@html description}
			</p>
		{/if}

		{#if starred}
			<img src="src/lib/assets/icons/star_outlined.png" alt="star" class="star w-10 absolute -top-4 -left-4"/>
		{/if}
	</div>
</button>

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
