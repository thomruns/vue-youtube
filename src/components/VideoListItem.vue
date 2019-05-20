<template>
    <li class="list-group-item media li-item">
      <img :src="thumbnailUrl" class="mr-3">
      <div class="media-body">
        {{ video.snippet.title }}
      </div>
    </li>
</template>

<script>
export default {
  name: 'VideoListItem',
  props: ['video'],
  data() {
    return {

    }
  },
  computed: {
    thumbnailUrl() {
      return this.video.snippet.thumbnails.default.url
    }
  }
}
</script>

<style>
.li-item {
  display: flex;
  cursor: pointer;
}
.li-item:hover {
  background-color: #eee;
}
</style>