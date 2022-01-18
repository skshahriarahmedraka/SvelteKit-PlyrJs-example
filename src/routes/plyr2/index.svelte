<script>
  import { Plyr } from "svelte-plyr";
  export let videoId;

//   function logEvent(event) {
//     console.log(event)
//   }

  let player


//   import { Plyr } from './components/components.module.js';
  let events = ['timeupdate']
  function logEvent(event) {
    console.log(event)
  }
</script>

<!-- <div class="youtube-plyr">
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
</style> -->

<Plyr on:timeupdate={logEvent} eventsToEmit={events}>
  <video
    crossorigin
    playsinline
    poster="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-HD.jpg"
    src="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-576p.mp4"
  >
    <source
      size="576"
      src="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-576p.mp4"
      type="video/mp4"
    >
    <source
      size="720"
      src="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-720p.mp4"
      type="video/mp4"
    >
    <source
      size="1080"
      src="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-1080p.mp4"
      type="video/mp4"
    >
    <track
      default
      kind="captions"
      label="English"
      src="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-HD.en.vtt"
      srclang="en"
    >
    <track
      kind="captions"
      label="Français"
      src="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-HD.fr.vtt"
      srclang="fr"
    >
    <a
      download=""
      href="https://cdn.plyr.io/static/demo/View_From_A_Blue_Moon_Trailer-576p.mp4"
    >
      Download
    </a>
  </video>
</Plyr>