<template>
  <div class="vlist-item">
    <li>{{ video.snippet.title }}</li>
  </div>
</template>

<script>
export default {
  name: 'VideoListItem',
  props: ['video'],
  data() {
    return {

    }
  }
}
</script>

<style>
.vlist-item {
  background-color: #e1b07e;
}
.vlist-item h1 {
  font-size: 1.4em;
  color: #eee;
}

</style>