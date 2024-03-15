<script lang="ts">
	import Group from '$lib/components/Group.svelte';
	import Control from '$lib/components/controlls/Control.svelte';

	// export let schema: any;
	// export let uischema: any;
	export let data: any;
	let compList: any[] = [];

	for (let i = 0; i < Object.keys(data).length; i++) {
		switch (typeof Object.values(data)[i]) {
			case 'string':
				compList.push([Control, { cType: 'text', label: Object.keys(data)[i] }]);
				break;

			case 'number':
				compList.push([Control, { cType: 'number', label: Object.keys(data)[i] }]);
				break;

			case 'boolean':
				compList.push([Control, { cType: 'boolean', label: Object.keys(data)[i] }]);
				break;

			// case 'object':
			// 	compList.push([Group, { label: Object.keys(data)[i]}, [Control, { cType: 'boolean', label: Object.keys(data)[i] }]]);
			// 	break;

			default:
				console.log(typeof Object.values(data)[i]);
				break;
		}
	}
</script>

{#each compList as [component, props, slotComponent]}
	<svelte:component this={component} {...props}>
        <!-- {slotComponent} -->
    </svelte:component>
{/each}
