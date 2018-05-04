<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <!-- <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1508/a5/4003f9dd7bebf61eccbf64046e26d487.water.jpg_600x330_a80ff353.jpg"/> -->
      <img class="banner-img" :src="bannerImg"/>
      <div class="banner-info">
        <div class="banner-title">
          {{ this.sightName }}
        </div>
        <div class="banner-num">
          <span class="iconfont banner-icon">&#xe632;</span>
          {{ this.gallaryImgs.length }}
        </div>
      </div>
    </div>
    <common-gallary
      :imgs="gallaryImgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'

export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    gallaryImgs: Array
  },
  data () {
    return {
      showGallary: false
      // imgs: ['http://img1.qunarzz.com/sight/p0/1804/c8/c88bb5e69c9a9c5ea3.img.jpg_r_800x800_0a55341c.jpg', 'http://img1.qunarzz.com/sight/p0/1804/78/781d085517106ccea3.img.jpg_r_800x800_ae5b774c.jpg']
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height 0.6rem
      color #fff
      background-image linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
        flex 1
        font-size 0.32rem
        padding 0 0.2rem
      .banner-num
        height 0.32rem
        line-height 0.32rem
        margin-top 0.14rem
        padding 0 0.4rem
        border-radius 0.2rem
        background rgba(0, 0, 0, .8)
        font-size 0.24rem
</style>
