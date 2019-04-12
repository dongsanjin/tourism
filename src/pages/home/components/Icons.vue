<template>
  <div class="icons">
    <div class="icon" v-for="item of iconList" :key="item.id">
      <div class="icon-img">
        <img class="icon-img-content" :src="item.imgUrl" alt="">
      </div>
      <p class="icon-desc">{{item.desc}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/48/cb72b99b71974c02.png',
        desc: '生活休闲'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
        desc: '亲子游'
      },
      {
        id: '0004',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/a40ee278d67000f2a29d2e20f6a029b3.png',
        desc: '自然风光'
      },
      {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
        desc: '踏青赏花'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .icons
    overflow hidden
    height 0
    padding-bottom 50%
    .icon
      position relative
      overflow hidden
      float left
      width 25%
      height 0
      padding-bottom 25%
      .icon-img
        position absolute
        top 0
        left 0
        right 0
        bottom .44rem
        box-sizing border-box
        padding .1rem
        .icon-img-content
          display block
          height 100%
          margin 0 auto
      .icon-desc
        position absolute
        left 0
        right 0
        bottom 0
        height .44rem
        line-height .44rem
        text-align center
        color $darkTextColor
</style>
