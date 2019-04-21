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
        <router-link tag="li" :to="'/details/' + list.id" class="location-info border-bottom" v-for="list of linkList" :key="list.id">
          <div class="location-wrapper">
            <div class="location-left">
              <img class="img-file" :src="list.imgUrl" alt="">
              <div class="img-bg bg-orange" v-if="list.bgOrange">{{list.time}}</div>
              <div class="img-bg bg-blue" v-else>{{list.time}}</div>
            </div>
            <div class="location-right">
              <p class="title">{{list.title}}</p>
              <p class="assess"><i class="iconfont star">&#xe600;&#xe600;&#xe600;&#xe600;&#xe600;</i><span class="sum">{{list.sum}}</span>评论</p>
              <p class="price"><span class="money-symbol money-color">￥</span><span class="money money-color">{{list.money}}</span>起<span class="area">{{list.area}}</span></p>
              <p class="location-merit" v-if="list.merit">在“海底两万里”鱼你共舞</p>
            </div>
          </div>
        </router-link>
      </ul>
    </section>
    <section class="more">
      查看所有产品
    </section>
  </div>
</template>
<script>
export default {
  name: 'HomeLink',
  props: {
    linkList: Array
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .wrapper
    background-color #fff
    margin-top .2rem
    padding .3rem .2rem 0
    overflow hidden
    .title
      font-size .32rem
      .img-box
        width .3rem
        display inline-block
        .img-desc
          width 100%
          vertical-align baseline
    .location
      overflow hidden
      margin-top .3rem
      .location-info
        padding .2rem 0
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
              background-size cover
              font-size .2rem
              line-height .38rem
              text-align center
              color #fff
            .bg-orange
              background-image url(https://img1.qunarzz.com/piao/fusion/1802/20/2ba6d10b17972e02.png)
            .bg-blue
              background-image:url(https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png)
            .img-file
              width 100%
          .location-right
            overflow hidden
            position relative
            flex 1
            margin .32rem .2rem 0
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
                margin-left -.04rem
            .area
              float right
            .location-merit
              overflow auto
              margin .5rem 0 0 .1rem
              line-height .4rem
              font-size .2rem
              color #f55
    .more
      font-size .28rem
      line-height .8rem
      color #00afc7
      text-align center
</style>
