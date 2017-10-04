# vue-simple-lightbox
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

    <lightbox
      id="mylightbox"
      :images="images"
      :image_class=" 'img-responsive img-rounded' "
      :album_class=" 'my-album-class' "
      :options="options">
    </lightbox>

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
          ],
          options : {
            closeText : 'X'
          }
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
| image_class | String | Class for each image |
| album_class | String | Class for album. i.e. Group of images (current lightbox)|
| options | Object | Options for lightbox (refer following table) |

----

## Options
| Property | Default | Type | Description |
| -------- | ------- | ---- | ----------- |
| sourceAttr | href | string | the attribute used for large images |
| overlay | true | bool | show an overlay or not |
| spinner | true | bool | show spinner or not |
| nav | true | bool | show arrow-navigation or not |
| navText | ['&larr;','&rarr;'] | array | text or html for the navigation arrows |
| captions | true | bool | show captions if availabled or not |
| captionSelector | 'img' | string | set the element where the caption is. Set it to "self" for the A-Tag itself |
| captionType | 'attr' | string | how to get the caption. You can choose between attr, data or text |
| captionsData | title | string | get the caption from given attribute |
| captionPosition | 'bottom' | string | the position of the caption. Options are top, bottom or outside (note that outside can be outside the visible viewport!) |
| captionDelay | 0 | int | adds a delay before the caption shows (in ms) |
| close | true | bool | show the close button or not |
| closeText | '×' | string | text or html for the close button |
| swipeClose | true | bool | swipe up or down to close gallery |
| showCounter | true | bool | show current image index or not |
| fileExt | 'png&#124;jpg&#124;jpeg&#124;gif' | regexp or false | list of fileextensions the plugin works with or false for disable the check |
| animationSpeed | 250 | int | how long takes the slide animation |
| animationSlide | true | bool | weather to slide in new photos or not, disable to fade |
| preloading | true | bool | allows preloading next und previous images |
| enableKeyboard | true | bool | allow keyboard arrow navigation and close with ESC key |
| loop | true | bool | enables looping through images |
| rel | false | mixed | group images by rel attribute of link with same selector.
| docClose | true | bool | closes the lightbox when clicking outside |
| swipeTolerance | 50 | int | how much pixel you have to swipe, until next or previous image |
| className: | 'simple-lightbox' | string | adds a class to the wrapper of the lightbox |
| widthRatio: | 0.8 | float | Ratio of image width to screen width |
| heightRatio: | 0.9 | float | Ratio of image height to screen height |
| disableRightClick | false | bool | disable rightclick on image or not |
| disableScroll | true | bool | stop scrolling page if lightbox is opened |
| alertError | true | bool | show an alert, if image was not found. If false error will be ignored |
| alertErrorMessage | 'Image not found, next image will be loaded' | string | the message displayed if image was not found |
| additionalHtml | false | string | Additional HTML showing inside every image. Usefull for watermark etc. If false nothing is added |
| history | true | bool | enable history back closes lightbox instead of reloading the page |

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
