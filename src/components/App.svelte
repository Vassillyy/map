<script>
  import Map from "./Map.svelte";
  import TileLayer from "./TileLayer.svelte";
  import View from "./View.svelte";
  import Link from "./Link.svelte";
</script>

<Map>
  <TileLayer slot="TileLayer" />
  <View slot="View" />
  <Link slot='Link' />
</Map>
