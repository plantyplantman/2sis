<script lang="ts">
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-rocket.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';

	import { AppShell, AppBar, Toast } from '@skeletonlabs/skeleton';
	import { Drawer, drawerStore } from '@skeletonlabs/skeleton';
	import type { DrawerSettings } from '@skeletonlabs/skeleton';

	import TwoSistersLogo from '$lib/icons/TwoSistersLogo.svelte';
	import HamburgerIcon from '$lib/icons/HamburgerIcon.svelte';

	const drawerSettings: DrawerSettings = {
		id: 'mobile-nav'
	};
</script>

<Toast />
<Drawer width="w-full">
	{#if $drawerStore.id === 'mobile-nav'}
		<div class="flex flex-col items-center">
			<div class="flex justify-center w-full">
				<TwoSistersLogo class="max-w-xs mb-4 mt-4" />
				<button class="btn btn-lg ml-auto" on:click={() => drawerStore.close()}>X</button>
			</div>
			<button class="btn btn-lg variant-filled-surface w-full">
				<a href="/location" class="w-full"> <span class="flex-auto">Location</span></a>
			</button>
			<hr />
			<button class="btn btn-lg variant-filled-surface w-full">
				<a href="/hours"> <span class="flex-auto">Hours</span></a>
			</button>
			<hr />
			<button class="btn btn-lg variant-filled-surface w-full">
				<a href="/about"> <span class="flex-auto">About </span></a>
			</button>
			<hr />
			<button class="btn btn-lg variant-filled-surface w-full">
				<a href="/contact"> <span class="flex-auto">Contact </span></a>
			</button>
			<hr />
			<button class="btn btn-lg variant-filled-surface w-full">
				<a href="/catering"> <span class="flex-auto">Catering </span></a>
			</button>
			<hr />
			<button class="btn btn-lg variant-filled-surface w-full">
				<a
					href="https://food.google.com/chooseprovider?restaurantId=/g/1vg4jz59&g2lbs=ALIxsqrTOPfBVdx3E-fl4ms0a0kZ-9_UybVc7TwJnylbnga5VLDtEcG8htYLBoZEGVz_tTRd7D4FpYBWw3-qDWWW7uLaxaNtpv85yNKdteKJtruYm-jCMVs%3D&hl=en-AU&gl=au&ssta=1&fo_m=MfohQo559jFvMWvkddHzV46uMT_RFPQ05bfKMQVr5-7IofUJMU_hT8vrWuwRMUv3d8yCO4PgMUOzJVpjPL1YMfZ3bInYwBDuMfaXTPp5KXh-&gei=f18AZJHjJYSM-AbI8Lr4Aw&ei=f18AZJHjJYSM-AbI8Lr4Aw&fo_s=OA,AH&orderType=2&sei=Cd-p6i5KI4WZEZbxVCS6K-eB"
				>
					<span class="flex-auto">Menu </span></a
				>
			</button>
			<hr />
			<button class="btn btn-lg variant-filled-surface w-full">
				<a href="/reservations"> <span class="flex-auto">Reserve </span></a>
			</button>
			<hr />
			<button class="btn btn-lg variant-filled-surface w-full">
				<a
					href="https://food.google.com/chooseprovider?restaurantId=/g/1vg4jz59&g2lbs=ALIxsqrTOPfBVdx3E-fl4ms0a0kZ-9_UybVc7TwJnylbnga5VLDtEcG8htYLBoZEGVz_tTRd7D4FpYBWw3-qDWWW7uLaxaNtpv85yNKdteKJtruYm-jCMVs%3D&hl=en-AU&gl=au&ssta=1&fo_m=MfohQo559jFvMWvkddHzV46uMT_RFPQ05bfKMQVr5-7IofUJMU_hT8vrWuwRMUv3d8yCO4PgMUOzJVpjPL1YMfZ3bInYwBDuMfaXTPp5KXh-&gei=f18AZJHjJYSM-AbI8Lr4Aw&ei=f18AZJHjJYSM-AbI8Lr4Aw&fo_s=OA,AH&orderType=2&sei=Cd-p6i5KI4WZEZbxVCS6K-eB"
				>
					<span class="flex-auto">Order </span></a
				>
			</button>
		</div>
	{/if}
</Drawer>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<figure>
					<a href="/">
						<TwoSistersLogo class="w-28" />
					</a>
				</figure>
			</svelte:fragment>

			<svelte:fragment slot="trail">
				<!-- <div class="relative hidden lg:block">
					<a class="btn btn-sm variant-ghost-surface" href="/about" rel="noreferrer"> About </a>
					<a
						class="btn btn-sm variant-ghost-surface"
						href="/reservations"
						target="_blank"
						rel="noreferrer"
					>
						Reserve
					</a>
					<a
						class="btn btn-sm variant-ghost-surface"
						href="https://food.google.com/chooseprovider?restaurantId=/g/1vg4jz59&g2lbs=ALIxsqrTOPfBVdx3E-fl4ms0a0kZ-9_UybVc7TwJnylbnga5VLDtEcG8htYLBoZEGVz_tTRd7D4FpYBWw3-qDWWW7uLaxaNtpv85yNKdteKJtruYm-jCMVs%3D&hl=en-AU&gl=au&ssta=1&fo_m=MfohQo559jFvMWvkddHzV46uMT_RFPQ05bfKMQVr5-7IofUJMU_hT8vrWuwRMUv3d8yCO4PgMUOzJVpjPL1YMfZ3bInYwBDuMfaXTPp5KXh-&gei=f18AZJHjJYSM-AbI8Lr4Aw&ei=f18AZJHjJYSM-AbI8Lr4Aw&fo_s=OA,AH&orderType=2&sei=Cd-p6i5KI4WZEZbxVCS6K-eB"
						rel="noreferrer"
					>
						Food
					</a>
				</div> -->

				<div class="relative block">
					<button class="btn btn-lg" on:click={() => drawerStore.open(drawerSettings)}>
						<HamburgerIcon class="w-8 h-8" />
					</button>
				</div>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<slot />
</AppShell>
