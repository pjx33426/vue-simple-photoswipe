## simple-photoswipe
A picture preview plugin based on Vue
## Installation
```
npm install --save vue-lunar-full-calendar
```
```js
//main.js
import simplePhotoswipe from 'simple-photoswipe'
Vue.use(simplePhotoswipe)
```

But you can also import the standalone component to add locally or for more complex installations.

```js
// foo.vue
import { simplePhotoswipe } from 'simple-photoswipe'
export default {
  components: {
    simplePhotoswipe
  },
}
```
## Methods 
```html
<simple-photoswipe :slides="slides" :options="options" @close="close" @next="next" @prev="prev"
      @goTo="goTo" @updateSize="updateSize"
       ref="simplePhotoswipe"></simple-photoswipe>
...
<script>
...
  data() {
    return {
      slides:[
          {
              src: 'https://img.zcool.cn/community/01ff2059770a25a8012193a37c7695.jpg@1280w_1l_2o_100sh.jpg',
              msrc:'https://img.zcool.cn/community/01ff2059770a25a8012193a37c7695.jpg@1280w_1l_2o_100sh.jpg',
              w: 964,
              h: 1024
          },
          {
              src: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1541502380130&di=9126f8939434001d6536c9d32bacffcb&imgtype=0&src=http%3A%2F%2Ftvax4.sinaimg.cn%2Fcrop.0.0.996.996.1024%2F006HxkHbly8flgt44j5rij30ro0rpacl.jpg',
              msrc: 'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1541502380130&di=9126f8939434001d6536c9d32bacffcb&imgtype=0&src=http%3A%2F%2Ftvax4.sinaimg.cn%2Fcrop.0.0.996.996.1024%2F006HxkHbly8flgt44j5rij30ro0rpacl.jpg',
              w: 964,
              h: 1024
          }
      ],
    }
  },
  
  methods: {
    close(){
        console.log('close')
    },
    next(){
        console.log('next')
    },
    prev(){
        console.log('prev')
    },
    goTo(index){
        console.log('goTo'+index)
    },
    updateSize(force){
        console.log('updateSize'+force)
    }
  },
...
</script>
```
## API document

[photoswipe docs](http://photoswipe.com/documentation/getting-started.html)

## Example App
I have created a simple Vue 2 webpack application as an example/playground
https://github.com/a306916069/vue-simple-photoswipe.git

