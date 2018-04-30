<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom" v-on:click="hello('当前城市')">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">{{this.$store.state.city}}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    cities: Object,
    hotCities: Array,
    letter: String
  },
  methods: {
    hello (city) {
      alert('hello' + city)
    }
  },
  mounted () {
    console.log(this.$refs.wrapper)
    this.scroll = new Bscroll(this.$refs.wrapper, {click: true})
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
    .border-topbottom
      &:before
        border-color #ccc
      &:after
        border-color #ccc
    .border-bottom
      &:before
        border-color #ccc
    .list
      overflow hidden
      position absolute
      left 0
      top 1.58rem
      right 0
      bottom 0
      .title
        line-height .54rem
        background #eee
        padding-left .2rem
        color #666
        font-size .26em
      .button-list
        overflow hidden
        padding .1rem .6rem .1rem .1rem
        .button-wrapper
          float left
          width 33.33%
          .button
            margin .1rem
            padding .1rem 0
            text-align center
            border .02rem solid #ccc
            border-radius .06rem
      .item-list
        .item
          line-height .76rem
          color #666
          padding-left .2rem
</style>
