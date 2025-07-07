<script>
	import Product from '$lib/ui/Product.svelte';
	import {base} from "$app/paths"
</script>

<svelte:head>
	<title>Products | No Sweat Soles</title>
</svelte:head>

<div class="mx-5 lg:mx-20">
	<h1 class="font-heading uppercase text-5xl lg:text-7xl text-darkest text-center lg:text-left my-12">Our Products</h1>
	<div class="grid grid-cols-1 lg:grid-cols-2 gap-4">
		<Product imgSrc="{base}/spray.webp" imgAlt="Natural Shoe Deodorizer Spray"
						 name="Natural Shoe Deodorizer Spray" quantity="8 oz"
						 price="$8.99"
						 oldPrice="$15.99"
						 preorder="https://buy.stripe.com/dRm5kC4MR2g6cI90IadEs00">
			Freshness that fights back — naturally.
			Made with essential oils and plant-based ingredients, this powerful spray eliminates shoe odor without harsh
			chemicals. Safe, non-toxic, and tough on funk — perfect for sneakers, cleats, or everyday shoes.
		</Product>
		<Product imgSrc="{base}/wipes.webp" imgAlt="Deodorizing Wipes" name="Deodorizing Wipes" quantity="20 wipes"
						 price="$5.99"
						 oldPrice="$8.99"
						 preorder="https://buy.stripe.com/dRm5kC4MR2g6cI90IadEs00">
			Clean soles, fresh steps. Anytime. Anywhere.
			These biodegradable wipes are infused with natural deodorizing agents and calming botanical extracts. Great for
			post-gym, summer sandals, or keeping your kicks crisp on the go.
		</Product>
	</div>
</div>