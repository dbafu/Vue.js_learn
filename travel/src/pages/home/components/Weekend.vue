<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" alt="" class="item-img">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b2/fde1bfcd057a52.jpg_r_640x214_bbf3fa44.jpg',
        title: '北京野生动物园 北京野生动物园 ',
        desc: '北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园  8689条评论'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b2/fde1bfcd057a52.jpg_r_640x214_bbf3fa44.jpg',
        title: '北京野生动物园 北京野生动物园 ',
        desc: '北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园  8689条评论'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b2/fde1bfcd057a52.jpg_r_640x214_bbf3fa44.jpg',
        title: '北京野生动物园 北京野生动物园 ',
        desc: '北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园  8689条评论'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b2/fde1bfcd057a52.jpg_r_640x214_bbf3fa44.jpg',
        title: '北京野生动物园 北京野生动物园 ',
        desc: '北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园  8689条评论'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/b2/fde1bfcd057a52.jpg_r_640x214_bbf3fa44.jpg',
        title: '北京野生动物园 北京野生动物园 ',
        desc: '北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园 北京野生动物园  8689条评论'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background-color #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
</style>
