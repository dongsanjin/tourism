<template>
  <div class="wrapper">
    <section class="service">
      <ul class="list-wrapper">
        <li class="service-list">
          <span class="iconfont icon-symbol">&#xe621;</span><a class="service-link" href="#">机票</a>
        </li>
        <li class="service-list">
          <span class="iconfont icon-symbol">&#xe680;</span><a class="service-link" href="#">酒店</a>
        </li>
        <li class="service-list">
          <span class="iconfont icon-symbol">&#xe609;</span><a class="service-link" href="#">火车</a>
        </li>
        <li class="service-list">
          <span class="iconfont icon-symbol">&#xe89d;</span><a class="service-link" href="#">更多</a>
        </li>
      </ul>
      <section class="personal">
        <ul>
          <li class="personal-list"><a href="#">登录</a></li>
          <li class="personal-list"><a href="#">我的订单</a></li>
          <li class="personal-list"><a href="#">最近浏览</a></li>
          <li class="personal-list"><a href="#">关于我们</a></li>
        </ul>
      </section>
    </section>
    <section class="select">
      <section class="select-version">
        <a class="version select-active" href="#">触屏版</a>
        <a class="version" href="#">电脑版</a>
      </section>
      <p class="icp">Qunar 京ICP备05021087<a class="icp-link" href="#">意见反馈</a></p>
    </section>
  </div>
</template>
<script>
export default {
  name: 'Footer'
}
</script>
<style lang="stylus" scoped>
  .wrapper
    overflow hidden
    margin-top .2rem
    .service
      margin-top .2rem
      border-bottom .02rem solid #cacaca
      .wraning-symbol
        font-size .16rem
        margin-right .1rem
        vertical-align text-top
      .list-wrapper
        width 76%
        display flex
        margin 0 auto
        color #000
        .service-list
          padding-left .2rem
          flex 1
          opacity .4
          .icon-symbol
            font-size .44rem
            float left
          .service-link
            margin-left .1rem
            font-size .2rem
            color inherit
            line-height .44rem
            border-bottom .02rem solid black
          &:last-child
            position relative
            .service-link
              border-bottom 0
              font-size .28rem
            &:before
              position absolute
              top 0
              left 0
              width .24rem
              height .24rem
            &:after
              position absolute
              left 0
              top 15%
              content: ""
              width .02rem
              height 70%
              background-color #000
      .personal
        padding .3rem .2rem
        .personal-list
          display inline-block
          padding 0 .2rem
    .select
      .select-version
        margin .2rem 0
        text-align center
        .version
          padding 0 .2rem
      .select-active
        color black
      .icp
        margin-bottom .2rem
        text-align center
        color #9e9e9e
        .icp-link
          color #9e9e9e
</style>
