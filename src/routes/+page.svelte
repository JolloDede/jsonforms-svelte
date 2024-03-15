<script lang="ts">
	import JsonForms from "$lib/JsonForms.svelte";
    import schema from "../schema.json";
    import uischema from "../uischema.json";

    let initialData = { name: 'Max Power', vegetarian: false, birthDate: "1985-06-02", handys: 3, personalData: { age: 34}, postalCode: "1234" };
</script>

<JsonForms 
    data={initialData}
/>

<!-- <JsonForms 
    schema={schema}
    uischema={uischema}
    data=""
/> -->