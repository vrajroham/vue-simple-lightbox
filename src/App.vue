<template>
<div id="app">
    <h1 class="title">Vue Lightbox</h1>
    <h4 class="desc">A wrapper around Simple Lightbox for Vue 2</h4>
    <Vuelightbox id="mylightbox"></Vuelightbox>
</div>
</template>

<script>
import Vuelightbox from '../src/index'
export default {
  name: 'MainApp',
  components: {
    Vuelightbox
  },
  mounted() {
    console.log("App Mounted");
  }
}
</script>

<style scoped>
@import 'https://fonts.googleapis.com/css?family=Roboto';
</style>
