<script>
    import TileLayer from "ol/layer/Tile";
    import OSM from "ol/source/OSM";
    import { onMount } from "svelte";
    import { getContext, setContext } from "svelte";

    let map = getContext("map");

    onMount(() => {
        if (map) {
            let layer = new TileLayer({
                source: new OSM(),
            });

            map.addLayer(layer);
        }
    });

</script>
