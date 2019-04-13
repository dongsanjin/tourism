<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont back-header">&#xe624;</div>
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
    text-align center
    color #fff
    font-size .32rem
    background-color $bgColor
    .back-header
      position absolute
      left 0
      top 0
      color #fff
      font-size .3.4rem
      font-weight bold
      margin-left .2rem
</style>
