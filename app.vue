<template>
  <div>
    <input v-model="url" type="text" />
    <button @click="playVideo">play</button>
    <div data-vjs-player>
      <video
        style="height: 100vh; width: 100vw"
        controls
        preload="auto"
        id="vid1"
        class="video-js"
      >
        <source :src="url" />
      </video>
    </div>
  </div>
</template>

<script setup lang="ts">
import videojs from "video.js";

const url = ref("");

const playVideo = () => {
  videojs("vid1");
};
</script>
