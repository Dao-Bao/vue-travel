<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" />
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
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    line-height: 2.5rem
    background: #eee
    text-indet: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 37.87%
    .item-img
      width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: 1.5rem
      ellipsis()
    .item-desc
      line-height: 2rem
      font-size: .8rem
      color: #ccc
      ellipsis()
</style>
