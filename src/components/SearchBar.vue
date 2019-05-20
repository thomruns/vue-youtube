<template>
  <div class="search">
    <input type="text" @keypress.enter="onEnter" placeholder="enter search term">
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  data() {
    return {

    }
  },
  methods: {
    onEnter(e) {
      this.$emit('termChange', e.target.value)
    }
  }
}
</script>

<style>
.search {
  text-align:center;
  margin: 20px;
}

.search input {
  width: 75%;
}



</style>