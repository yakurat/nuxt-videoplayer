<template>
  <section class="container">
    <video-player :options="videoOptions"></video-player>
  </section>
</template>

<script>
import VideoPlayer from '@/components/VideoPlayer.vue';
import 'video.js/dist/video-js.css';

export default {
  components: {
    VideoPlayer
  },
  data() {
    return {
      videoOptions: {
        autoplay:true,
        controls: true,
        sources: [
          {
            src: '/static/hoge.webm',
            type: 'video/webm'
          }
        ]
      }
    }
  }
}
</script>
