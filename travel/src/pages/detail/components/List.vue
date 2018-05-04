<template>
  <div>
    <div class="item" v-for="(item, index) of list" :key="index">
      <div class="item-title border-bottom">
        <span class="item-title-icon"></span>
        {{item.title}}
      </div>
      <div v-if="item.children" class="item-children">
        <detail-list :list="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .item-title
    line-height 0.8rem
    font-size 0.32rem
    padding 0 0.2rem
    .item-title-icon
      position relative
      left 0.02rem
      top 0.06rem
      display inline-block
      width 0.36rem
      height 0.36rem
      background: url('~img/tb.png') 0 0 no-repeat
      margin-right 0.1rem
      background-size .36rem .36rem
  .border-bottom
    border-bottom 1px solid #000000
  .item-children
    padding 0 0.2rem
</style>
