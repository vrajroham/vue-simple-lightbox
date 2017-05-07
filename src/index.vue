<template>
  <div>
    <div class="my-gallery" :class="album_class">
      <a :href="image.src" v-for="image,key in images">
        <img :src="image.src" alt="" :title="image.title" :class="image_class" />
      </a>
    </div>
  </div>
</template>

<script>
  export default{
    props:{
      id : {
        type :  String,
        required : true
      },
      images : {
        type : Array,
        required : true
      },
      image_class : {
        type : String
      },
      album_class : {
        type : String
      }
    },
    mounted(){      
      try {
          window.$ = window.jQuery = require('jquery');
          var simplelightbox = require('simplelightbox');
          var gal = $('.my-gallery a').simpleLightbox()
      } catch (e) {}
    }
  }
</script>

<style>
  .my-gallery a img {
    float: left;
    width: 20%;
    height: auto;
    border: 2px solid #fff;
    -webkit-transition: -webkit-transform .15s ease;
    -moz-transition: -moz-transform .15s ease;
    -o-transition: -o-transform .15s ease;
    -ms-transition: -ms-transform .15s ease;
    transition: transform .15s ease;
    position: relative;
  }
  .my-gallery a:hover img {
    -webkit-transform: scale(1.05);
    -moz-transform: scale(1.05);
    -o-transform: scale(1.05);
    -ms-transform: scale(1.05);
    transform: scale(1.05);
    z-index: 5;
  }
 .my-gallery a.big img {
    width: 40%;
  }

  .align-center {
    text-align: center;
  }

  @import url('https://fonts.googleapis.com/css?family=Ruda');
  @import "~simplelightbox/dist/simplelightbox.css";

</style>
