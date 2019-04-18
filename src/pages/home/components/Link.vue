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
        <li class="location-info">
          <div class="location-left">
            <img class="img-file" src="http://img1.qunarzz.com/sight/p0/1504/47/4730a0c01664b63d.water.jpg_200x200_d7f52253.jpg" alt="">
            <div class="img-bg">可订明日</div>
          </div>
          <div class="location-right">
            <p>武汉海昌极地海洋公园</p>
            <p><i></i><span></span>评论</p>
            <p>￥<span></span>起</p>
          </div>
          <div class="location-merit">

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
</style>
