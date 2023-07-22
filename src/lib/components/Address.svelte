<script lang="ts">
	import { clipboard } from '@skeletonlabs/skeleton';
	import { toastStore } from '@skeletonlabs/skeleton';
	import type { ToastSettings } from '@skeletonlabs/skeleton';
	import ClipboardIcon from '$lib/icons/ClipboardIcon.svelte';

	const address = '5/38 Badham St, Dickson ACT 2602';
	const toastMessage = 'Address copied to clipboard';

	const toastSettings: ToastSettings = {
		message: toastMessage
	};
</script>

<div class="mt-4">
	<span class="border border-slate-200/10 p-2">
		5/38 Badham St, Dickson ACT 2602
		<button
			use:clipboard={address}
			on:click={() => toastStore.trigger(toastSettings)}
			class="btn-[sm] variant-outline-secondary p-1 rounded-sm"
		>
			<ClipboardIcon />
		</button>
	</span>
</div>
