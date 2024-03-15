<script lang="ts">
	import BooleanControl from "./BooleanControl.svelte";
	import NumberControl from "./NumberControl.svelte";
	import TextControl from "./TextControl.svelte";

    export let cType: string;
    export let label: string;
</script>

<div>
    {#if cType == "text"}
        <TextControl {label} />
    {/if}
    {#if cType == "number"}
        <NumberControl {label} />
    {/if}
    {#if cType == "boolean"}
        <BooleanControl {label} />
    {/if}
</div>