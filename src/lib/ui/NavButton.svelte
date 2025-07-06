<script lang="ts">
	import type { Snippet } from 'svelte';

	interface Props {
		children: Snippet;
		href: string;
		class?: string;
	}

	let { children, href, class: clazz = '' }: Props = $props();
</script>

<a {href}
	 class="flex lg:flex-col items-center lg:justify-between py-8 hover:bg-darker p-2 gap-2 transition-background duration-100 {clazz}">
	{@render children()}
</a>
