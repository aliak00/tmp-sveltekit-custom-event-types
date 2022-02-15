<script>
	import Component from '$lib/Component.svelte';
</script>

<Component
	on:declaredType={(e) => {
		console.log(e.detail.gagagaga);
	}}
	on:inlineType={(e) => {
		console.log(e.detail.gagagaga);
	}}
/>
