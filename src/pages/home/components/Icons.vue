<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
    <div class="icon"
         v-for="item of page"
         :key="item.id">
      <div class="icon-img">
       <img class="icon-image-content" :src="item.imgurl">
      </div>
      <p class="icon-desc">{{ item.desc }}</p>
    </div>
      </swiper-slide>
    </swiper>
   </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconsList: [{
        id: '0001',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '0002',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        desc: '一日游'
      }, {
        id: '0003',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        desc: '成都必游'
      }, {
        id: '0004',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/e3/67df61427c8e1302.png',
        desc: '川剧变脸'
      }, {
        id: '0005',
        imgurl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '自然风光'
      }, {
        id: '0006',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1805/57/1e29afd06f881102.png',
        desc: '稻城亚丁'
      }, {
        id: '0007',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
        desc: '游乐场'
      }, {
        id: '0008',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png',
        desc: '熊猫基地'
      }, {
        id: '0009',
        imgurl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        desc: '动植物园'
      }, {
        id: '00010',
        imgurl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/f04285731d7121da1b9028e2bf431695.png',
        desc: '都江堰'
      }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  @import "~styles/mixins.styl"
  .icons >>> .swiper-container
    height :0
    padding-bottom :50%
    .icon
      position :relative
      overflow :hidden
      float :left
      width :25%
      padding-bottom :25%
      .icon-img
        position :absolute
        top :0
        right :0
        left :0
        bottom :.44rem
        box-sizing :border-box
        padding :.1rem
        .icon-image-content
          display :block
          margin :0 auto
          height :100%
      .icon-desc
        position :absolute
        left :0
        right :0
        bottom :0
        height: .44rem
        line-height: .44rem
        text-align :center
        color :$darkTextColor
        ellipse()
</style>
