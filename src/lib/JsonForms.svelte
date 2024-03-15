<script lang="ts">
	import DefaultRenderer from './renderer/DefaultRenderer.svelte';

	// export let schema: any;
	// export let uischema: any;
	export let data: any;
	// export let renderers: any = ;
	// export let cells: Object;
	// export let onChange: {};
</script>

<DefaultRenderer {data} />

<!-- <DefaultRenderer {schema} {uischema} {data} /> -->

