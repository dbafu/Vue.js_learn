<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ab/2d291e6cf2bc7f02.jpg_640x200_fa5f0167.jpg'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/1b/6c766b79e2045102.jpg_640x200_3e44c74a.jpg'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/15/9250dbc86a456302.jpg_640x200_4c7220d4.jpg'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/c905d7879e288802.jpg_640x200_36a02c62.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff !important
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 31.25%
    background #eee
    .swiper-img
      width 100%
</style>
