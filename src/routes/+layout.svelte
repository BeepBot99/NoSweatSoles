<script lang="ts">
	import '../app.css';
	import Nav from '$lib/ui/Nav.svelte';

	let { children } = $props();
</script>

<Nav />

{@render children()}

<div class="bg-darker py-16 text-light mt-16 text-center">
	<p class="text-xl">&copy; 2025 No Sweat Soles. All rights reserved.</p>
	<p class="text-md text-light/50 pt-3">Website made by <a class="text-accent hover:underline"
																													 target="_blank"
																													 href="https://github.com/BeepBot99">Davis Luxenberg</a>.</p>
</div>