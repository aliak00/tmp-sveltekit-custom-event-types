<script context="module" lang="ts">
	type Events = {
		event1: {
			value: string;
		};
	};
</script>

<script lang="ts">
	import { createEventDispatcher } from 'svelte';
	const dispatch1 = createEventDispatcher<Events>();
	const dispatch2 = createEventDispatcher<{
		event2: {
			value: string;
		};
	}>();
</script>

<button on:click={() => dispatch1('event1', { value: 'hello' })}>
	Dispatch with declared type
</button>

<button on:click={() => dispatch2('event2', { value: 'hello' })}>
	Dispatch with inline type
</button>
