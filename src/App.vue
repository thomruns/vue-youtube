<template>
  <div id="app">
    <h1 id="app-title">YouTube Video Browser App</h1>
    <SearchBar></SearchBar>
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
  background-color: #aaa6ac;
}
#app-title {
  padding: 20px;
  font-size: 1.4em;
  text-transform: uppercase;
}
</style>
