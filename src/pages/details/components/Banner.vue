<template>
  <div>
    <div class="img-wrapper">
      <router-link to="/album">
        <img class="img-file" src="//img1.qunarzz.com/sight/p0/1501/10/1012e4a2c398409c.water.jpg_600x330_3321a6b0.jpg" alt="">
      </router-link>
      <router-link tag="div" to="/" class="back-header iconfont">&#xe624;</router-link>
      <div class="img-info">
        <p class="img-num"><span class="iconfont">&#xe859;</span>19</p>
        <div class="img-title">云雾山(AAAAA景区)</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Banner'
}
</script>
<style lang="stylus" scoped>
  .img-wrapper
    position relative
    overflow hidden
    width 100%
    height 0
    padding-bottom 55%
    .img-file
      width 100%
    .back-header
      position absolute
      top .2rem
      left .2rem
      width .6rem
      height .6rem
      line-height .6rem
      border-radius .3rem
      color #fff
      text-align center
      font-weight bold
      background-color rgba(0,0,0,.5)
    .img-info
      overflow hidden
      position absolute
      bottom 0
      left 0
      right 0
      height 1.2rem
      z-index 1
      .img-num
        width 1.2rem
        height .4rem
        line-height .4rem
        margin-left .2rem
        text-align center
        color #fff
        border-radius .2rem
        background-color rgba(0,0,0,.5)
      .img-title
        padding-left .2rem
        margin-top .1rem
        width 100%
        color #fff
        font-size .36rem
    &:after
      position absolute
      left 0
      bottom 0
      content: ''
      display block
      width 100%
      height .6rem
      background-image linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,.8))
</style>
