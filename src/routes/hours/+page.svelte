<script>
	import Hours from '$lib/components/Hours.svelte';
	import TwoSistersLogo from '$lib/icons/TwoSistersLogo.svelte';
	import Cta from '$lib/components/CTA.svelte';
</script>

<div class="flex flex-col items-center text-center">
	<span>
		<TwoSistersLogo class="md:max-w-[70vw] mb-8 mt-4" />
		<h1 class="h1">Opening Hours</h1>
	</span>
	<Hours class="md:max-w-[70vw] mt-4" />
	<Cta class="mt-4" />
</div>
