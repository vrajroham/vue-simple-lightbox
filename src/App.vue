<template>
  <div id="app">
      <h1 class="title">Vue Lightbox</h1>
      <h4 class="desc">A wrapper around Simple Lightbox for Vue 2</h4>
      <Vuelightbox id="mylightbox" :items="items" img_class="imgs df"></Vuelightbox>
  </div>
</template>

<script>
import Vuelightbox from '../src/index'
export default {
  name: 'MainApp',
  components: {
    Vuelightbox
  },
  data(){
    return{
      items : ['http://andreknieriem.de/sl/demo/images/thumbs/thumb1.jpg','http://andreknieriem.de/sl/demo/images/thumbs/thumb2.jpg','http://andreknieriem.de/sl/demo/images/thumbs/thumb3.jpg']
    }
  },
  mounted() {
    console.log("App Mounted");
    console.log(this.items);
  }
}
</script>

<style>
@import 'https://fonts.googleapis.com/css?family=Roboto';

.imgs.df{
  padding-left: 20px;
}
</style>
