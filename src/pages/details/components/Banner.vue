<template>
  <div>
    <div class="img-wrapper">
      <router-link to="/album">
        <img class="img-file" src="//img1.qunarzz.com/sight/p0/1501/10/1012e4a2c398409c.water.jpg_600x330_3321a6b0.jpg" alt="">
      </router-link>
      <div class="img-info">
        <p class="img-num"><span class="iconfont">&#xe859;</span>19</p>
        <div class="img-title">云雾山(AAAAA景区)</div>
      </div>
    </div>
    <section class="Attractions-info">
      <section class="info-wrapper">
        <div class="evaluation-box">
          <p class="evaluation"><span class="fraction">4.8</span>分 很棒</p>
          <p class="desc">1318条评论</p>
          <span class="iconfont more">&#xe643;</span>
        </div>
        <div class="introduction-box">
          <p class="introduction">景点简介</p>
          <p class="desc">开放时间、贴士</p>
          <span class="iconfont more">&#xe643;</span>
        </div>
      </section>
      <section class="location">
        <span class="iconfont location-icon">&#xe601;</span>
        湖北省武汉市黄陂区泡桐店境内
        <span class="iconfont more">&#xe643;</span>
      </section>
    </section>
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
  .Attractions-info
    overflow hidden
    position absolute
    z-index 2
    margin-top -.1rem
    width 100%
    border-radius .1rem .1rem 0 0
    background-color #fff
    .info-wrapper
      display flex
      .evaluation-box,
      .introduction-box
        position relative
        top 0
        left 0
        margin .2rem
        flex 1
        .fraction
          font-size .4rem
        .more
          position absolute
          top 20%
          right 0
        .desc
          font-size .2rem
          margin-top .1rem
        .evaluation
          color #ff8300
        .introduction
          margin-top .1rem
      .introduction-box:after
        position absolute
        left -.2rem
        top 0
        content:''
        display block
        width 1px
        height 100%
        background-color #e0e0e0
        transform scaleX(.3333)
    .location
      position relative
      padding .2rem
      &:before
        position absolute
        top 0
        left 5%
        content: ''
        display block
        height 1px
        width 90%
        transform scaleY(.33333)
        background-color #e0e0e0
      .location-icon
        margin-right .1rem
      .more
        float right
</style>
