<template>
  <div class="video-list">
    <h1>Video List Component</h1>
    <ul>
      <li v-for="(video, index) in videos" :key="index">{{video.snippet.title}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'VideoList',
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