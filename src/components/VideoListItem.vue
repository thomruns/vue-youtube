<template>
    <li class="list-group-item">{{ video.snippet.title }}</li>
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

</style>