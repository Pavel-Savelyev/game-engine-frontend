<script>
    import ToolBar from "./lib/ToolBar.svelte";
    import AssetBrowser from "./lib/AssetBrowser.svelte";
    import Scenes from "./lib/Scenes.svelte";
    import MainContent from "./lib/MainContent.svelte";
    import StatusBar from "./lib/StatusBar.svelte";
</script>
<main>
    <div class="container-fluid">
        <div class="row">
            <div class="col-auto col-md-3 col-xl-2 px-sm-2 px-0 bg-dark">
                <Scenes></Scenes>
            </div>
            <div class="col p-0">
                <ToolBar></ToolBar>
                <MainContent></MainContent>
                <StatusBar></StatusBar>
            </div>
            <div class="col-auto col-md-3 col-xl-2 px-sm-2 px-0 bg-dark">
                <AssetBrowser></AssetBrowser>
            </div>
        </div>
    </div>
</main>