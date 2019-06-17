<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
        <router-link
          tag="li"
          class="item border-bottom"
          v-for="item of list"
          :key="item.id"
          :to="'/detail/' + item.id"
        >
            <img
              class="item-img"
              :src="item.imgUrl"
            />
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button
              class="item-button"
            >查看详情</button>
          </div>
        </router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: 0
    line-height: 2.5rem
    background: #eee
    text-indet: .2rem
  .item
    overflow: hidden
    display: flex
    height: 6rem
    .item-img
      width: 5.5rem
      height: 5.5rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: 1.5rem
        ellipsis()
      .item-desc
        line-height: 2rem
        font-size: .8rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: 1.2rem
        margin-top: .2rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        font-size: .8rem
        color: #fff
</style>
