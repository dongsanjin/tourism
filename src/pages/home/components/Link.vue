<template>
  <div class="wrapper">
    <section class="title">
      <div class="img-box">
        <img class="img-desc" src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="">
      </div>
      猜你喜欢
    </section>
    <section class="location">
      <ul>
        <li class="location-info border-bottom">
          <div class="location-wrapper">
            <div class="location-left">
              <img class="img-file" src="http://img1.qunarzz.com/sight/p0/1504/47/4730a0c01664b63d.water.jpg_200x200_d7f52253.jpg" alt="">
              <div class="img-bg">可订明日</div>
            </div>
            <div class="location-right">
              <p class="title">武汉海昌极地海洋公园</p>
              <p class="assess"><i class="iconfont star">&#xe600;&#xe600;&#xe600;&#xe600;&#xe600;</i><span class="sum">19067</span>评论</p>
              <p class="price"><span class="money-symbol money-color">￥</span><span class="money money-color">180</span>起<span class="area">东西湖区</span></p>
              <p class="location-merit">在“海底两万里”鱼你共舞</p>
            </div>
          </div>
        </li>
      </ul>
    </section>
  </div>
</template>
<script>
export default {
  name: 'HomeLink'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .wrapper
    height 50vh
    background-color #fff
    margin-top .2rem
    padding .3rem .2rem
    overflow hidden
    box-sizing border-box
    .title
      font-size .32rem
      .img-box
        width .3rem
        display inline-block
        .img-desc
          width 100%
          vertical-align baseline
    .location
      margin-top .5rem
      .location-info
        .location-wrapper
          display flex
          overflow hidden
          .location-left
            float left
            width 2rem
            position relative
            .img-bg
              position absolute
              top 0
              left 0
              width 1.02rem
              height .38rem
              background-image url('https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png')
              background-size cover
              font-size .2rem
              line-height .38rem
              text-align center
              color #fff
            .img-file
              width 100%
          .location-right
            overflow hidden
            position relative
            flex 1
            margin .32rem .2rem .2rem
            .title
              font-size .32rem
            .assess
              margin-top .2rem
              font-size .1rem
              .star
                color $moneyColor
                font-size .1rem
                vertical-align text-top
                margin-right .3rem
            .price
              overflow hidden
              margin .3rem 0 .2rem
              font-size .2rem
              width 100%
              .money-color
                color $moneyColor
              .money
                font-size .4rem
                margin-left -.1rem
            .area
              float right
            .location-merit
              overflow auto
              margin .5rem 0 0 .1rem
              line-height .4rem
              font-size .2rem
              color #f55
</style>
