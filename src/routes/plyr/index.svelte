<script>
  import { Plyr } from "svelte-plyr";
  export let videoId;

  function logEvent(event) {
    console.log(event)
  }

  let player
</script>

<div class="youtube-plyr">
  <button on:click={() => player.play()}>PLAY</button>
  <button on:click={() => player.pause()}>PAUSE</button>
  <Plyr on:timeupdate={logEvent} bind:player={player}>
    <div class="plyr__video-embed">
      <iframe
        src="https://www.youtube.com/watch?v=DS1WUcx5sMc"
        allowfullscreen allowtransparency allow="autoplay">
      </iframe>
    </div>
  </Plyr>
</div>

<style>
.youtube-plyr {
  max-width: 800px;
}
</style>