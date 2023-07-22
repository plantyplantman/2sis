<script>
	import Address from '$lib/components/Address.svelte';
	import Map from '$lib/components/Map.svelte';
	import Cta from '$lib/components/CTA.svelte';
</script>

<div class="flex flex-col items-center text-center py-4">
	<h1 class="h1">Two Sisters Lao Thai Cuisine Location</h1>
	<Address />

	<div
		class="card mt-4 max-w-xs md:max-w-xl p-4 bg-gradient-to-br variant-gradient-primary-secondary"
	>
		<p>
			Nestled in the vibrant heart of Dickson, Canberra, Two Sisters Lao Thai Cuisine is your
			gateway to an unforgettable culinary journey. <br />Our restaurant is conveniently located
			amidst the bustling city life, making it an ideal spot for both locals and visitors to indulge
			in authentic Lao and Thai flavours.
		</p>
	</div>
	<Map class="max-w-xs md:max-w-xl mt-4" />
	<Cta class="mt-4" />
</div>
