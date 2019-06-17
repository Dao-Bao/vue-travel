<template>
  <div>
    <div
      class="item"
      v-for="(item,index) of list"
      :key="index"
    >
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
  .item-title-icon
    position: relative
    left: .2rem
    top: .06rem
    display: inline-block
    width: 1.2rem
    height: 1.2rem
    background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat
    margin-right: .1rem
    background-size: .4rem 3rem
  .item-title
    line-height: 2.5rem
    font-size: 1.0rem
    padding: 0 .2rem
  .item-children
    padding: 0 .6rem
</style>
