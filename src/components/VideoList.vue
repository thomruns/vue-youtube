<template>
  <div class="video-list col-md-4">
    <ul class="list-group">
      <VideoListItem v-for="video in videos"
      :key="video.etag"
      :video="video"
      @videoSelect="onVideoSelect"
      ></VideoListItem>
    </ul>
  </div>
</template>

<script>
import VideoListItem from './VideoListItem'

export default {
  name: 'VideoList',
  components: {
    VideoListItem
  },
  props: {
    videos: Array
  },
  methods: {
    onVideoSelect(video) {
      this.$emit('videoSelect', video)
    }
  }

}
</script>

<style>
.video-list {
  text-align: left;
}
.video-list h1 {
  font-size: .4em;
  color: #eee;
}

</style>