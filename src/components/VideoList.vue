<template>
  <div class="video-list">
    <h1>Video List Component</h1>
    <ul>
      <VideoListItem v-for="(video, index) in videos" :key="index"></VideoListItem>
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
}
.video-list h1 {
  font-size: 1.4em;
  color: #eee;
}

</style>