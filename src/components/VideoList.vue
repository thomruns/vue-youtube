<template>
  <div class="video-list">
    <h1>Video List Component</h1>
    <ul class="list-group">
      <VideoListItem v-for="video in videos"
      :key="video.etag"
      :video="video"
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
  }

}
</script>

<style>
.video-list {
  background-color: #af6596;
  text-align: left;
}
.video-list h1 {
  font-size: .4em;
  color: #eee;
}

</style>