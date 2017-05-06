<template>
  <div id="app">
      <Vuelightbox id="mylightbox" :images="items"></Vuelightbox>
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
        items : [
          {
              src : 'http://andreknieriem.de/sl/demo/images/thumbs/thumb1.jpg',
              title : 'Image 2'
          },
          {
              src : 'http://andreknieriem.de/sl/demo/images/thumbs/thumb2.jpg',
              title : 'Image 3'
          },
          {
              src : 'http://andreknieriem.de/sl/demo/images/thumbs/thumb3.jpg',
              title : ''
          },
          {
              src : 'http://andreknieriem.de/sl/demo/images/thumbs/thumb4.jpg',
              title : ''
          },
        ]
      }
    },
    mounted() {

    }
  }
</script>

<style>

</style>
