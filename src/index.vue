<template>
</template>

<script>
  export default{
    props:{
      id : {
        type :  String,
        required : true
      }
    },
    mounted(){
      try {
          window.$ = window.jQuery = require('jquery');
          var simplelightbox = require('simplelightbox');
      } catch (e) {}
    }
  }
</script>

<style scoped></style>
