<script>
    import TileLayer from "ol/layer/Tile";
    import { useGeographic } from "ol/proj";
    import OSM from "ol/source/OSM";
    import { onMount } from "svelte";
    import { getContext } from "svelte";

    let map = getContext("map");

    onMount(() => {
        if (map) {
            const layer = new TileLayer({
                source: new OSM(),
            });

            map.addLayer(layer);
        }
    });
</script>
