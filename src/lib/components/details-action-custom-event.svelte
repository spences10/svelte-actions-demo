<script lang="ts">
	import { confetti } from '@neoconfetti/svelte';
	import { tick } from 'svelte';

	export let text = '';
	export let open = false;
	let isVisible = false;

	// custom slide animation
	const slide = (node: HTMLDivElement, open: boolean) => {
		let initialHeight = node.offsetHeight;
		node.style.height = open ? `auto` : '0px';
		node.style.overflow = 'hidden';
		let animation = node.animate(
			[{ height: '0px' }, { height: `${initialHeight}px` }],
			{
				duration: 200,
				easing: 'ease-in-out',
				fill: 'both',
				direction: open ? 'reverse' : 'normal',
			},
		);
		animation.pause();
		animation.onfinish = ({ currentTime }) => {
			if (currentTime === 0) {
				animation.reverse();
				animation.pause();
			}
			node.dispatchEvent(new CustomEvent('animationEnd'));
		};
		return {
			update: () => {
				animation.currentTime
					? animation.reverse()
					: animation.play();
			},
		};
	};
</script>

<section class="not-prose border-primary rounded-lg border-4">
	<button
		aria-controls="accordion__content_3"
		aria-expanded={open}
		tabindex="0"
		id="accordion__title_3"
		on:click={() => {
			open = !open;
		}}
	>
		<div class="flex items-center text-left">
			<span style="margin:0 1rem;" class="transition" class:open>
				▶
			</span>
			<p style="margin:1rem 0;">{text}</p>
		</div>
	</button>
	<div
		use:slide={open}
		on:animationEnd={async () => {
			isVisible = false;
			await tick();
			isVisible = true;
		}}
	>
		<slot />
	</div>
	{#if isVisible}
		<div class="flex items-center justify-center">
			<div use:confetti></div>
		</div>
	{/if}
</section>

<style>
	.open {
		transform: rotate(90deg);
		transform-origin: center;
	}
</style>
