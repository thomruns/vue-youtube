<template>
  <div id="app">
    <div id="ytl"><img src="./assets/youtube-logo.png" alt="YouTube Logo"></div>
    <h2 id="app-title">Video Browser App</h2>
    <SearchBar @termChange="onUserEnter"></SearchBar>
    <VideoDetail></VideoDetail>
    <VideoList></VideoList>
    <VideoListItem></VideoListItem>
  </div>
</template>

<script>
import SearchBar from './components/SearchBar.vue'
import VideoDetail from './components/VideoDetail.vue'
import VideoList from './components/VideoList.vue'
import VideoListItem from './components/VideoListItem.vue'

export default {
  name: 'App',
  components: {
    SearchBar,
    VideoDetail,
    VideoList,
    VideoListItem
  },
  data() {
    return {

    }
  },
  methods: {
    onUserEnter(searchTerm) {
      window.console.log('you searched for:', searchTerm)
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
