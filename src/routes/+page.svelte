<script>
    import Summary from "./summary.svelte";
    import Section from "./section.svelte";
    import {sections} from '../objects'
</script>

<Summary />
{#each sections as section}
    <Section content={section} />
{/each}


<style>

</style>
