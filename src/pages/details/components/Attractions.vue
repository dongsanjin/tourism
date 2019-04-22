<template>
  <div class="Attractions-info">
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
    </div>
</template>
<script>
export default {
  name: 'Attractions'
}
</script>
<style lang="stylus" scoped>
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
