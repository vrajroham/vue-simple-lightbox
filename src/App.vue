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
              src : 'https://cdn.rawgit.com/vrajroham/vrajroham.github.io/85d64ac5/imgs/img1.jpg',
              title : 'Image 2'
          },
          {
              src : 'https://cdn.rawgit.com/vrajroham/vrajroham.github.io/85d64ac5/imgs/img2.jpg',
              title : 'Image 3'
          },
          {
              src : 'https://cdn.rawgit.com/vrajroham/vrajroham.github.io/85d64ac5/imgs/img3.jpg',
              title : ''
          },
          {
              src : 'https://cdn.rawgit.com/vrajroham/vrajroham.github.io/85d64ac5/imgs/img4.jpg',
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
