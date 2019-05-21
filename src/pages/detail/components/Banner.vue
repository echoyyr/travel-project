<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img  class="banner-img"  :src='bannerImg'>
      <div class="banner-info">
        <div class="banner-title">{{this.sightName}}</div>
        <div>
          <div class="banner-number"><span class="iconfont banner-icon">&#xe77c;</span>{{this.gallaryImgs.length}}</div>
        </div>
      </div>
    </div>
    <common-gallary :imgs="gallaryImgs" v-show="showGallary" @close="handleGallaryClick"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
import Detail from '../Detail'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201309/24/977fea7b3c5cd758c8d65eac.jpg_r_800x800_3755d9a0.jpg', 'http://img1.qunarzz.com/sight/p0/201309/24/977fea7b3c5cd758c8d65eac.jpg_r_800x800_3755d9a0.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClick () {
      this.showGallary = false
    }
  },
  components: {
    Detail,
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    width 100%
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      color #fff
      display flex
      position absolute
      right 0
      bottom 0
      left 0
      background-image  linear-gradient(top,rgba(0, 0, 0, 0),rgba(0, 0, 0, 0.8))
      line-height .6rem
      .banner-title
        flex 1
        font-size .32rem
        padding  0 .2rem
      .banner-number
        height .32rem
        line-height .32rem
        margin-top .14rem
        padding 0 .4rem
        border-radius .2rem
        font-size .24rem
        background rgba(0, 0, 0, .8)
        .banner-icon
          font-size .24rem
</style>
