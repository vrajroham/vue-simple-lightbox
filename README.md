# vue-simple-lightbox [WIP]
A Vue.js component for touch-friendly image lightbox for mobile and desktop powered by [Simple Lighbox](https://github.com/andreknieriem/simplelightbox)

**[LIVE DEMO](http://andreknieriem.de/sl/demo/)**

---
## Install
````
// For Vue.js 2.0+
npm install vue-simple-lightbox
````
## Usage
1. Import the module
2. Register it as a component as you would any other Vue component
3. Use it within your template

### Example
````vue
<template>
  <div id="app">
    <p>Welcome to your Vue.js lightbox!</p>

    <lightbox id="mylightbox" :images="images"></lightbox>

  </div>
</template>

<script>
  import Lightbox from 'vue-simple-lightbox'

  export default {
    components: {
      Lightbox
    },
    data(){
        return{
          images : [
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
      }
  }
</script>
````

## Props
Many of these props are inherited from [simplelightbox configuration so see their docs](https://github.com/andreknieriem/simplelightbox#javascript-options) for further details.

| Prop Name | Type | Description |
|----------|------|--------------|
| id | String | A string by which to identify the component, can be anything. **Required**|
| images | Array | Array containing (src,title) **Required** |

----

**Basic lightbox. More options, features and improvements are in devlopment mode.**

---

## Development

``` bash
# install dependencies
npm install

# serve example at localhost:8080
npm run dev

# build any changes made
npm run build
```
