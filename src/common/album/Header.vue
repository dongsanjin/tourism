<template>
  <div class="wrapper">
    <router-link tag="div" to="/details/:id" class="iconfont back-details">&#xe624;</router-link>
    <div class="title">景区图片</div>
  </div>
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style lang="stylus" scoped>
  .wrapper
    overflow hidden
    position fixed
    top 0
    left 0
    right 0
    width 100%
    height 0
    line-height 1rem
    text-align center
    font-size .32rem
    background-color #fff
    padding-bottom 1rem
    .back-details
      position absolute
      left .2rem
      top 0
      font-size .5rem
      font-weight bold
</style>
