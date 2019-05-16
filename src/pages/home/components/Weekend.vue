<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item" border-bottom v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgurl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}} </p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgurl: 'http://img1.qunarzz.com/sight/source/1505/a2/78e4dbcfd45a6d.jpg_r_640x214_7a62b06a.jpg',
        title: '成都必打卡',
        desc: '成都的标志，也是现代人对老成都的记忆'
      }, {
        id: '0002',
        imgurl: 'http://img1.qunarzz.com/sight/source/1811/65/7322301be0a92c.jpg_r_640x214_a3485c55.jpg',
        title: '摩崖石刻造像',
        desc: '诸事不顺，来抱佛脚，中国最壮观的大佛大盘点~来一场真正的“佛”系之旅，乐山大佛是首选'
      }, {
        id: '0003',
        imgurl: 'http://img1.qunarzz.com/sight/source/1505/63/0ffcb5c329a19c.jpg_r_640x214_93fd1e5a.jpg',
        title: '成都文艺范儿',
        desc: '《成都》唱火了这里，其实这儿不只有酒馆，还有很多文艺爆棚的地方'
      }, {
        id: '0004',
        imgurl: 'http://img1.qunarzz.com/sight/source/1505/63/0ffcb5c329a19c.jpg_r_640x214_93fd1e5a.jpg',
        title: '玩转主题乐园',
        desc: '乐园，与青春作伴'
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
  .item-img-wrapper
    padding-bottom :33.9%
    height :0
    overflow: hidden
    .item-img
      width :100%
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
</style>
