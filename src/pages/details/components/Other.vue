<template>
  <div class="other-wrapper">
    <div class="title">
      看了该景点的人还看了
    </div>
    <div>
      <ul>
        <li class="other-list" v-for="(list, index) of otherlist" :key="index">
          <div class="img-box">
            <img class="img-tag" :src="list.imgUrl" alt="">
          </div>
          <div class="info-box">
            <div class="price">
              <span class="money">￥<strong class="money-num">{{list.moneyNum}}</strong></span>起
            </div>
            <div class="info-title">
              {{list.title}}<span class="level">{{list.level}}</span>
            </div>
            <div class="assess">
              <span class="iconfont star">&#xe600;&#xe600;&#xe600;&#xe600;&#xe600;</span>
              <span class="assess-num">{{list.assessNum}}条评论</span>
            </div>
            <div class="area">{{list.area}}</div>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Other',
  props: {
    otherlist: Array
  }
}
</script>
<style lang="stylus" scoped>
.other-wrapper
  margin-top .2rem
  background-color #fff
  .title
    position relative
    height .88rem
    line-height .88rem
    font-size .3rem
    padding-left .4rem
    &:before
      content: ''
      display block
      position absolute
      top 50%
      left .1rem
      width .06rem
      height .3rem
      transform translateY(-50%)
      background-color #1ba9ba
    &:after
      content: ''
      display block
      position absolute
      bottom 0
      left 0
      width 100%
      height 1px
      border-top 1px solid #dadada
      transform scaleY(.33333)
  .other-list
    position relative
    overflow hidden
    display flex
    padding .2rem 0 .2rem .2rem
    .img-box
      width 1.62rem
      height 1.62rem
      float left
      .img-tag
        width 100%
        height 100%
    .info-box
      position relative
      float left
      flex 1
      margin-left .2rem
      padding-right .2rem
      .price
        float right
        font-size .2rem
        .money
          color #ff9800
          .money-num
            font-size .36rem
            font-weight 400
      .info-title
        font-size .3rem
        .level
          color #adadad
      .assess
        margin-top .3rem
        font-size .2rem
        color #adadad
        .star
          color #ffb436
          font-size .2rem
        .assess-num
          margin-left .2rem
      .area
        margin-top .4rem
        font-size .2rem
        color #adadad
        text-indent .1rem
      &:after
        content: ''
        display block
        width 100%
        height 1px
        background-color #adadad
        transform scaleY(.33333)
        position absolute
        bottom -.2rem
        left 0
</style>
