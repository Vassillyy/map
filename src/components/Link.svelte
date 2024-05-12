<script>
    import Link from "ol/interaction/Link";
    import { onMount } from "svelte";
    import { getContext } from "svelte";

    let map = getContext("map");

    onMount(() => {
        if (map) {
            map.addInteraction(new Link());
        }
    });
    
</script>
