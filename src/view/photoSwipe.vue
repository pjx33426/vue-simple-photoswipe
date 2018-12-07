<template>
  <div class="photoSwipe">
    <simple-photoswipe :slides="slides"
                       :options="options"
                       @close="close"
                       @afterChange="afterChange"
                       @beforeChange="beforeChange"
                       @destroy="destroy"
                       ref="simplePhotoswipe"></simple-photoswipe>
  </div>
</template>
<script>
import { simplePhotoswipe } from 'simple-photoswipe'
export default {
  data: function () {
    return {
      slides: [
        {
          src: 'https://img.zcool.cn/community/01ff2059770a25a8012193a37c7695.jpg@1280w_1l_2o_100sh.jpg',
          msrc: 'https://img.zcool.cn/community/01ff2059770a25a8012193a37c7695.jpg@1280w_1l_2o_100sh.jpg',
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
      options: {
        index: 0,
        shareEl: false
      }
    }
  },
  components: {
    simplePhotoswipe
  },
  methods: {
    close () {
      console.log('close')
    },
    afterChange () {
      console.log('afterChange')
    },
    beforeChange () {
      console.log('beforeChange')
    },
    goTo (index) {
      console.log('goTo' + index)
    },
    destroy () {
      console.log('destroy')
    }

  }
}
</script>
<style scoped lang="scss">
.photoSwipe {
  /deep/ {
    figure {
      float: left;
      margin: 0 10px 0 0;
      padding: 0;
      width: 300px;
      height: 300px;
    }
    img {
      width: 300px;
      height: 300px;
    }
  }
}
</style>
