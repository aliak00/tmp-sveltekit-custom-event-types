<script context="module" lang="ts">
	type Events = {
		declaredType: {
			value: string;
		};
	};
</script>

<script lang="ts">
	import { createEventDispatcher } from 'svelte';
	const dispatch1 = createEventDispatcher<Events>();
	const dispatch2 = createEventDispatcher<{
		inlineType: {
			value: string;
		};
	}>();
</script>

<button on:click={() => dispatch1('declaredType', { value: 'hello' })}>
	Dispatch with declared type
</button>

<button on:click={() => dispatch2('inlineType', { value: 'hello' })}>
	Dispatch with inline type
</button>
