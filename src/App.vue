<template>
  <div id="app" class="container">
    <div id="ytl"><img src="./assets/youtube-logo.png" alt="YouTube Logo"></div>
    <h2 id="app-title">Video Browser App</h2>
    <SearchBar @termChange="onUserEnter"></SearchBar>
    <div class="row">
      <VideoDetail :video="selectedVideo"></VideoDetail>
      <VideoList @videoSelect="onVideoSelect" :videos="videos"></VideoList>
    </div>
  </div>
</template>

<script>
const API_KEY ="API_KEY_HERE"
const YOUTUBE_URL = "https://www.googleapis.com/youtube/v3/search"
import axios from 'axios'
import SearchBar from './components/SearchBar.vue'
import VideoList from './components/VideoList.vue'
import VideoDetail from './components/VideoDetail.vue'

export default {
  name: 'App',
  components: {
    SearchBar,
    VideoList,
    VideoDetail
  },
  data() {
    return {
      videos: [],
      selectedVideo: null
    }
  },
  methods: {
    onUserEnter(searchTerm) {
      axios.get(YOUTUBE_URL, {
        params: {
          key: API_KEY,
          type: 'video',
          part: 'snippet',
          q: searchTerm
        }
      }).then(response => {
          this.videos = response.data.items
      })//window used to prevent
        .catch(err => window.console.log(err))// linting errors
    },
    onVideoSelect(video) {
        this.selectedVideo = video
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0;
  background-color: #e2dee4;
}
#app-title {
  font-size: 1.4em;
}
#ytl img {
  display: inline-block;
  padding: 10px;
}
</style>
