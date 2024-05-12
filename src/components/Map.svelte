<script>
  import { onMount } from "svelte";
  import Map from "ol/Map";
  import { setContext } from "svelte";
  import { useGeographic } from "ol/proj";

  let map;

  onMount(() => {
    useGeographic();
    map = new Map({
      target: "map",
    });
  });

  setContext("map", map);
</script>

<div id="map">
   <slot name='TileLayer'></slot>
   <slot name='View'></slot>
   <slot name='Link'></slot>
</div>

<style>
  #map {
    width: 100%;
    height: 400px;
  }
</style>
