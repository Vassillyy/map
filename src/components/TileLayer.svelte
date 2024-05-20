<script>
    import TileLayer from "ol/layer/Tile";
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

    // let layer
    // if (map) {
    //     layer = new TileLayer({
    //         source: new OSM(),
    //     })
    // }
    // onMount(() => {
    //     map.addLayer(layer);
    // })


    // let layer
    // onMount(() => {
    //     if (map) {
    //         layer = new TileLayer({
    //             source: new OSM(),
    //         })
    //     }
    // })
    // map.addLayer(layer);

</script>
