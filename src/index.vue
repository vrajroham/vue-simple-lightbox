<template>
  <ul>
    <img :src="i" v-for="i in items" alt="" :class="img_class">
  </ul>
</template>

<script>
  export default{
    props:{
      id : {
        type :  String,
        required : true
      },
      items : {
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
      } catch (e) {}
    }
  }
</script>

<style scoped></style>
