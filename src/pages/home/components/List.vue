<template>
  <div class="outer-wrapper">
    <section class="top">
      <section class="popular">
        <div class="img-wrapper">
          <img class="img-tag" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="">
        </div>
        <span class="popular-title">本周热门榜单</span>
      </section>
      <section class="all">
        全部榜单<i class="iconfont">&#xe643;</i>
      </section>
    </section>
    <section class="swiper">
    </section>
  </div>
</template>

<script>
export default {
  name: 'HomeList'
}
</script>

<style lang="stylus" scoped>
  .outer-wrapper
    padding 0.1rem
    .top
      background-color #f5f5f5
      overflow hidden
      .popular
        float left
        height .8rem
        line-height .8rem
        .img-wrapper
          width .3rem
          float left
          .img-tag
            vertical-align baseline
            width 100%
        .popular-title
          font-size .32rem
          padding-left .1rem
      .all
        float right
        height .8rem
        line-height .8rem
        padding-right .3rem
      &::after
        content: ''
        display block
        height 0
        clear both
</style>
