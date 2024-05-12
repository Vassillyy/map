<script>
  import { onMount } from "svelte";
  import { Map, View } from "ol";
  import { setContext } from "svelte";
  import { useGeographic } from "ol/proj";

  let map;

  onMount(() => {
    useGeographic();
    map = new Map({
      target: "map",
      view: new View({
        center: [0, 0],
        zoom: 3,
      }),
    });
  });

  setContext("map", map);
</script>

<div id="map">
  <slot />
</div>

<style>
  #map {
    width: 100%;
    height: 400px;
  }
</style>
