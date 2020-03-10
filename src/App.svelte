<script>
    import Home from './Home.svelte'
    import Video from './Videoplayer.svelte'

    import { Router, Link, Route } from "svelte-routing";

    export let url = "";
</script>

<main>
    <Router url="{url}">
        <nav>
            <Link to="/">Home</Link>
            <Link to="video">Video</Link>
        </nav>
        <div>
            <Route path="/"><Home /></Route>
            <Route path="video"><Video /></Route>
        </div>
    </Router>
</main>

<style>
	
</style>