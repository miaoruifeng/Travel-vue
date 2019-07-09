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
        <img class="item-img" :src="item.imgUrl" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
    margin-top .2rem
    line-height .68rem
    text-indent .2rem
    background #eee
  .item
    display flex
    overflow hidden
    height 1.9rem
    .item-img
      width 1.6rem
      height 1.6rem
      padding .15rem
    .item-info
      flex 1
      padding .15rem
      padding-left .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #bbb
        ellipsis()
      .item-button
        margin-top .16rem
        line-height .4rem
        padding 0 .2rem
        background #ff9300
        border-radius .06rem
        font-size .26rem
        color #fff
</style>
