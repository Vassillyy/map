<script>
  import { onMount } from "svelte";
  import Map from "ol/Map";
  import { setContext } from "svelte";
  import { useGeographic } from "ol/proj";

  let map;

  onMount(() => {
    useGeographic();
    map = new Map({
      target: "map-cont",
    });
  });

  setContext("map", map);
</script>

<div id="map-cont">
  <slot name="TileLayer"></slot>
  <slot name="View"></slot>
  <slot name="Link"></slot>
</div>

<style>
  #map-cont {
    width: 100%;
    height: 400px;
  }
</style>
