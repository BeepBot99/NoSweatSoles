<script lang="ts">
	import type { Snippet } from 'svelte';

	interface Props {
		imgSrc: string;
		imgAlt: string;
		name: string;
		quantity: string;
		price: string;
		children: Snippet;
		preorder: string;
		oldPrice?: string;
	}

	let { imgSrc, imgAlt, name, price, children, quantity, preorder, oldPrice }: Props = $props();
</script>

<div class="md:h-100 flex flex-col md:flex-row">
	<img class="max-h-full border-6 border-darkest/80" src={imgSrc} alt={imgAlt}>
	<div class="md:border-t-2 border-r-2 border-l-2 md:border-l-0 border-dark/80 flex-1 flex flex-col justify-between">
		<div class="p-4">
			<div class="font-heading tracking-wide uppercase mb-2">
				<h2>
					<span class="text-darker font-bold text-3xl">{name}</span>
					<span class="text-dark/80 text-xl">{quantity}</span>
				</h2>
				{#if oldPrice}
					<span class="text-dark/50 text-lg"><del>{oldPrice}</del></span>
				{/if}
				<span class="text-dark/80 text-2xl">{price}</span>
			</div>
			<p>
				{@render children()}
			</p>
		</div>
		<a href={preorder} target="_blank"
			 class="bg-darkest py-4 px-6 font-heading uppercase text-2xl tracking-wide text-light transition-colors duration-150 hover:bg-light border-y-2 border-darkest hover:border-y-dark/80 hover:text-darkest">Preorder
			Now</a>
	</div>
</div>