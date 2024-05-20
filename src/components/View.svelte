<script>
    import { View } from "ol";
    import { fromLonLat } from "ol/proj";  
    import { onMount } from "svelte";
    import { getContext } from "svelte";

    let map = getContext("map");

    onMount(() => {
        if (map) {
            const view = new View({
                center: fromLonLat([0, 0]),
                zoom: 3,
            });

            map.addView(view);
        }
    })

    // let view;
    // if (map) {
    //     view = new View({
    //         center: fromLonLat([0, 0]),
    //         zoom: 3,
    //     })
    // }
    // onMount(() => {
    //     map.addView(view);
    // })

    

</script>