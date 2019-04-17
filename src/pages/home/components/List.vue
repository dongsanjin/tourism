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
    <div class="scroll-wrapper">
      <div class="flex-box" ref="flexBox">
        <ul class="scroll-box">
          <li class="scroll-list">
            <div class="img-box">
              <img class="image" alt="">
            </div>
            <div class="img-desc">
              <p>户部巷</p>
              <p><span class="money">￥</span><em class="money money-num">65</em>起</p>
            </div>
          </li>
          <li class="scroll-list">
            <div class="img-box">
              <img class="image" alt="">
            </div>
            <div class="img-desc">
              <p>武汉东湖风景区</p>
              <p><span class="money">￥</span><em class="money money-num">32</em>起</p>
            </div>
          </li>
          <li class="scroll-list">
            <div class="img-box">
              <img class="image" alt="">
            </div>
            <div class="img-desc">
              <p>黄鹤楼</p>
              <p><span class="money">￥</span><em class="money money-num">65</em>起</p>
            </div>
          </li>
          <li class="scroll-list">
            <div class="img-box">
              <img class="image" alt="">
            </div>
            <div class="img-desc">
              <p>东湖樱园</p>
              <p><span class="money">￥</span><em class="money money-num">32</em>起</p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'

export default {
  name: 'HomeList',
  methods: {
    addScroll () {
      var srcoll = new BScroll(this.$refs.flexBox, {
        scrollX: true
      })
    }
  },
  mounted () {
    this.addScroll()
  }
}
</script>

<style lang="stylus" scoped>
  .outer-wrapper
    padding 0.1rem
    background-color #fff
    margin-top .2rem
    .top
      background-color #fff
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
        font-size .24rem
        color #333
      &::after
        content: ''
        display block
        height 0
        clear both
    .scroll-wrapper
      background-color #fff
      margin-top .2rem
      height 0
      padding-bottom 2.9rem
      background-size cover
      .flex-box
        overflow hidden
        height 2.9rem
        .scroll-box
          height 100%
          width auto
        .scroll-list
          position relative
          float left
          width 2rem
          height 100%
          margin 0 .16rem
          background-size contain
          background-repeat no-repeat
          .image
            max-width 100%
          .img-desc
            position absolute
            bottom .1rem
            width 100%
            font-size .24rem
            line-height .36rem
            text-align center
            .money
              font-size .24rems
              color #ff8300
            .money-num
              font-size .28rem
              margin-left -.04rem
          &:nth-child(1)
            background-image url('http://img1.qunarzz.com/sight/p0/201403/11/1f70100804193c28f8b71378c0faa49e.jpg_250x250_719a8492.jpg')
          &:nth-child(2)
            background-image url('http://img1.qunarzz.com/sight/p0/1603/56/56758da4c81e45d990.img.png_250x250_8a58d459.png')
          &:nth-child(3)
            background-image url('http://img1.qunarzz.com/sight/p0/1503/55/5577ab22b2e205d0.water.jpg_250x250_25866cfb.jpg')
          &:nth-child(4)
            background-image url('http://img1.qunarzz.com/sight/p0/1903/fe/feea19ebd8ed685ba3.img.jpg_250x250_c56db033.jpg')
</style>
