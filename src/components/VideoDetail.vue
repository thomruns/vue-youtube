<template>
  <div v-if="video" class="col-md-8">
    <div class="embed-responsive embed-responsive-16by9">
      <iframe class="embed-responsive-item" :src="videoURL"></iframe>
    </div>
    <div class="details">
      <h4>{{ video.snippet.title }}</h4>
      <p>{{ video.snippet.description }}</p>
    </div> 
  </div>
</template>

<script>
export default {
  name: 'VideoDetail',
  props: ['video'],
  data() {
    return {
    }
  },
  computed: {
    videoURL() {
      const videoID = this.video.id.videoId
      return `https://www.youtube.com/embed/${videoID}`
    }
  }
}
</script>

<style>
.details {
 background-color: #86a397;
  margin-top: 10px;
  padding: 10px;
  border: 1px solid #aaa;
  border-radius: 4px;
}


</style>