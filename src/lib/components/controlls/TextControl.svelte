<script context="module">
	let counter = 0;
</script>

<script lang="ts">
	export let label: string;
	let inputId = 'input_text_' + counter++;
</script>

<label for={inputId}>{label}</label>
<input id={inputId} type="text" />
