<template>
  <div class="wrapper">
    <div class="title">
      用户评价
    </div>
    <section class="assess">
      <ul>
        <li class="assess-wrapeer" v-for="user of userList" :key="user.id">
          <div class="assess-header">
            <span class="assess-star iconfont"><span class="good">&#xe600;&#xe600;&#xe600;&#xe600;&#xe600;</span></span>
            <span class="assess-user">{{user.name + ' ' + user.time}}</span>
          </div>
          <p class="assess-desc" :ref="user.id">{{user.desc}}</p>
          <div class="expand iconfont iconicon"></div>
          <div class="imgs-wrapper">
            <ul>
              <li class="img-list" v-for="(list, index) of user.imgsList" :key="index">
                <img class="img-tag" :src="list.imgUrl">
              </li>
            </ul>
          </div>
        </li>
      </ul>
    </section>
    <section class="all-assess">
      查看全部评论<span class="iconfont">&#xe643;</span>
    </section>
  </div>
</template>
<script>
export default {
  name: 'Assess',
  props: {
    userList: Array
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper
    overflow hidden
    margin-top .1rem
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
    .assess-wrapeer
      position relative
      padding .2rem
      margin-bottom .2rem
      &:before
        content: ''
        display block
        position absolute
        top 0
        left 0
        height 1px
        width 100%
        border-bottom 1px solid #e0e0e0
        transform scaleY(.33333)
      .assess-header
        overflow hidden
        padding-top .1rem
        font-size .2rem
        .assess-star
          float left
          font-size .26rem
          .good
            color orange
        .assess-user
          float right
      .assess-desc
        overflow hidden
        margin-top .2rem
        font-size .26rem
        color #616161
        height 2rem
        line-height .4rem
      .expand
        text-align center
        font-size .4rem
        margin-bottom .2rem
      .imgs-wrapper
        overflow hidden
        .img-list
          float left
          width 33%
          margin-bottom .1rem
          padding 0 .05rem
          box-sizing border-box
          .img-tag
            width 100%
    .all-assess
      position relative
      height .8rem
      line-height .8rem
      text-align center
      &:before
        content: ''
        display block
        position absolute
        top 0
        left 0
        height 1px
        width 100%
        border-top 1px dashed #dadada
        transform scaleY(.33333)
</style>
