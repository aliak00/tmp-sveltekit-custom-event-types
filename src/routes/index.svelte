<script>
	import Component from '$lib/Component.svelte';
</script>

<Component
	on:event1={(e) => {
		console.log(e.detail.gagagaga);
	}}
	on:event2={(e) => {
		console.log(e.detail.gagagaga);
	}}
/>
