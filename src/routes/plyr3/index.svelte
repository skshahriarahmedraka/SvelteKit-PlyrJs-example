<script lang="ts">
    import {Plyr} from "svelte-plyr"
    export let videoId
    let player
    let events=['timeupdate']
    function logEvent(event){
        console.log(event)
    }
    // your script goes here
</script>

<style>
    /* your styles go here */
</style>

<!-- markup (zero or more items) goes here -->

<Plyr on:timeupdate={logEvent} eventsToEmit={events}>
    <video   poster="video/one.jpg" src="video/cartoon.mp4">
    <track kind="captions" src="" type="video/mp4">
</video>
</Plyr>