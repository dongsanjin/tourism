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
        全部榜单<i class="iconfont right">&#xe643;</i>
      </section>
    </section>
    <div class="scroll-wrapper">
      <div class="flex-box" ref="flexBox">
        <ul class="scroll-box" ref="scrollBox">
          <li class="scroll-list" ref="scrollList" v-for="item in scrollItem" :key="item.id">
            <!-- 通过判断是否是前三景点，控制top图标的渲染 -->
            <template v-if="item.topUrl">
              <div class="top-box">
                <img class="top-list" :src="item.topUrl" alt="">
              </div>
            </template>
            <div class="img-box">
              <img class="img-list" :src="item.imgUrl" alt="">
            </div>
            <div class="img-info">
              <p class="img-desc">{{item.desc}}</p>
              <p><span class="money">￥</span><em class="money money-num">{{item.money}}</em>起</p>
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
  props: {
    scrollItem: Array
  },
  data () {
    return {
      liSum: 0,
      ulWidth: 0,
      liWidth: 116
    }
  },
  methods: {
    addScroll () {
      let srcoll = new BScroll(this.$refs.flexBox, {
        scrollX: true,
        eventPassthrough: 'vertical',
        bounce: false,
        momentum: true,
        scrollbar: {
          fade: true,
          interactive: false
        }
      })
      let scrollBox = this.$refs.scrollBox
      let timer = setInterval(() => {
        this.liSum = scrollBox.childElementCount
        if (this.liSum) {
          clearInterval(timer)
          this.setUlWidth()
        }
      }, 500)
    },
    setUlWidth () {
      let scrollBox = this.$refs.scrollBox
      this.ulWidth = this.liWidth * this.liSum
      scrollBox.style.width = this.ulWidth + 'px'
    }
  },
  mounted () {
    this.addScroll()
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .outer-wrapper >>> .bscroll-indicator
    height 80% !important
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
        padding-right .2rem
        font-size .24rem
        color #333
        .right
          font-size .34rem
          font-weight bold
          color #616161
      &::after
        content: ''
        display block
        height 0
        clear both
    .scroll-wrapper
      background-color #fff
      margin-top .2rem
      height 0
      padding-bottom 3rem
      background-size cover
      .flex-box
        position relative
        height 3rem
        .scroll-box
          height 100%
          width 158vh
        .scroll-list
          position relative
          display inline-block
          width 2rem
          height 100%
          margin 0 .16rem
          background-size contain
          background-repeat no-repeat
          .top-box
            position absolute
            width .84rem
            top -.06rem
            z-index 1
            .top-list
              width 100%
          .img-box
            position absolute
            top 0
            left 0
            width 2rem
            height 2rem
            .img-list
              width 100%
          .image
            max-width 100%
          .img-info
            position absolute
            bottom .2rem
            width 100%
            font-size .24rem
            line-height .36rem
            text-align center
            .img-desc
              ellipsis()
            .money
              font-size .24rems
              color #ff8300
            .money-num
              font-size .28rem
              margin-left -.04rem
</style>
