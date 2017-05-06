<template>
  <div class="container">
    <div class="gallery" v-for="image,key in images">
      <a :href="image.src" :class="{'big' : key == 0}"><img :src="image.src" alt="" :title="image.title" /></a>
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
        type : Array
      },
      img_class : {
        type : String
      }
    },
    mounted(){
      console.log(this.items);
      try {
          window.$ = window.jQuery = require('jquery');
          var simplelightbox = require('simplelightbox');
          var gal = $('.gallery a').simpleLightbox()
      } catch (e) {}
    }
  }
</script>

<style>
/*  a img {
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

  a:hover img {
    -webkit-transform: scale(1.05);
    -moz-transform: scale(1.05);
    -o-transform: scale(1.05);
    -ms-transform: scale(1.05);
    transform: scale(1.05);
    z-index: 5;
  }*/


  /* line 8, ../sass/demo.scss */
  * {
    box-sizing: border-box;
  }

  /* line 12, ../sass/demo.scss */
  a {
    color: #4ab19a;
  }

  /* line 16, ../sass/demo.scss */
  .clear {
    clear: both;
    float: none;
    width: 100%;
  }

  /* line 22, ../sass/demo.scss */
  .container {
    max-width: 1170px;
    width: 100%;
    padding-right: 15px;
    padding-left: 15px;
    margin-right: auto;
    margin-left: auto;
  }
  /* line 32, ../sass/demo.scss */
  .container .gallery a img {
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
  /* line 46, ../sass/demo.scss */
  .container .gallery a:hover img {
    -webkit-transform: scale(1.05);
    -moz-transform: scale(1.05);
    -o-transform: scale(1.05);
    -ms-transform: scale(1.05);
    transform: scale(1.05);
    z-index: 5;
  }
  /* line 57, ../sass/demo.scss */
  .container .gallery a.big img {
    width: 40%;
  }

  /* line 65, ../sass/demo.scss */
  .align-center {
    text-align: center;
  }



  @import url('https://fonts.googleapis.com/css?family=Ruda');
  @import "~simplelightbox/dist/simplelightbox.css";

</style>
