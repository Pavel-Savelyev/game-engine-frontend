<canvas id="main-content"></canvas>

<script>
    import {onMount} from "svelte";
    onMount(() => {
        const go = new Go();
        WebAssembly.instantiateStreaming(fetch("/wasm/main.wasm"), go.importObject).then((result) => {
            go.run(result.instance);
        }).catch(err => {
            console.error("Error loading WASM:", err);
        });
    })
</script>

<style>
    #main-content {
        border: solid 1px darkorange;
    }
</style>