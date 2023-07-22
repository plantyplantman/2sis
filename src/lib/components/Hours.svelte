<script lang="ts">
	import { Table, tableMapperValues } from '@skeletonlabs/skeleton';
	import type { TableSource } from '@skeletonlabs/skeleton';

	const hours = [
		{ position: 1, day: 'Monday', lunch: 'closed', dinner: '5-9:30pm' },
		{ position: 2, day: 'Tuesday', lunch: '11:30am-2:30pm', dinner: '5-9:30pm' },
		{ position: 3, day: 'Wednesday', lunch: '11:30am-2:30pm', dinner: '5-9:30pm' },
		{ position: 4, day: 'Thursday', lunch: '11:30am-2:30pm', dinner: '5-9:30pm' },
		{ position: 5, day: 'Friday', lunch: '11:30am-2:30pm', dinner: '5-9:30pm' },
		{ position: 6, day: 'Saturday', lunch: 'closed', dinner: '5-9:30pm' },
		{ position: 7, day: 'Sunday', lunch: 'closed', dinner: '5-9:30pm' }
	];

	const hoursSource: TableSource = {
		head: ['Day', 'Lunch', 'Dinner'],
		body: tableMapperValues(hours, ['day', 'lunch', 'dinner'])
	};
</script>

<div class={$$props.class}>
	<Table source={hoursSource} />
</div>
