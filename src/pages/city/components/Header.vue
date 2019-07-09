<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont city-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
    .header
      position relative
      overflow hidden
      height $headerHeight
      line-height $headerHeight
      background $bgColor
      text-align center
      font-size .32rem
      color #fff
      .city-back
        position absolute
        top 0
        left 0
        width .72rem
        text-align center
        font-size .36rem
        color #fff
</style>
