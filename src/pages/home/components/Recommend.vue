<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item" border-bottom v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgurl">
        <div class="item-info">
          <p class="item-title">{{item.title}} </p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
        title: '成都海昌极地海洋公园',
        desc: '浪漫成都首站，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
        title: '成都海昌极地海洋公园',
        desc: '浪漫成都首站，浪漫的海洋主题乐园'
      }, {
        id: '0003',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
        title: '成都海昌极地海洋公园',
        desc: '浪漫成都首站，浪漫的海洋主题乐园'
      }, {
        id: '0004',
        imgurl: 'http://img1.qunarzz.com/sight/p0/1612/1d/1d9a740c1f9e0efaa3.img.jpg_200x200_63285bd9.jpg',
        title: '成都海昌极地海洋公园',
        desc: '浪漫成都首站，浪漫的海洋主题乐园'
      }]
    }
  }
}

</script>
<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top :.2rem
    line-height: .8rem
    background : #eee
    text-indent :.2rem
  .item
    display :flex
    height :1.9rem
    overflow: hidden
    .item-img
      width :1.7rem
      height:1.7rem
      padding :0.1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0;
      .item-title
        ellipse()
        line-height :.54rem
        font-size :.32rem
      .item-desc
        ellipse()
        line-height :.4rem
        color :#ccc
      .item-button
        line-height :.44rem
        margin-top :.16rem
        background: #FB8900
        padding :0  .2rem
        border-radius :.06rem
        color :#fff
</style>
